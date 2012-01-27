=========================
PHPMD Supressing Warnings
=========================

You can use doc comment annotations to exclude methods or classes 
from PHPMD or to suppress special rules for some software artifacts. ::

  /**
   * This will suppress all the PMD warnings in
   * this class.
   *
   * @SuppressWarnings(PHPMD)
   */
  class Bar {
      function  foo() {
          $baz = 23;
      }
  }

Or you can suppress one rule with an annotation like this: ::

  /**
   *
   */
  class Bar {
      /**
       * This will suppress UnusedLocalVariable
       * warnings in this method
       *
       * @SuppressWarnings(PHPMD.UnusedLocalVariable)
       */
      public function foo() {
          $baz = 42;
      }
  }


A doc comment can contain multiple ``@SuppressWarnings`` annotations,
so that you can exclude multiple rules by name. ::

  /**
   * Suppress all warnings from these two rules.
   *
   * @SuppressWarnings(PHPMD.LongVariable)
   * @SuppressWarnings(PHPMD.UnusedLocalVariable)
   */
  class Bar {
      public function foo($thisIsALongAndUnusedVariable)
      {

      }
  }
