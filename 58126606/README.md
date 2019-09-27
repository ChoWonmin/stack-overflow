# How to traverse DOM to find the last ancestor with specific attribute in Javascript?

Here is my sample HTML:

``` html
<div id="parent1" data-attribute="parent">
  <div id="child2" data-attribute="child">
    <div id="grandchild4" data-attribute="child">
    </div>
  </div>
</div>
<div id="parent2" data-attribute="parent">
  <div id="child3" data-attribute="child">
    <div id="grandchild1" data-attribute="parent">
      <div id="item1"></div>
    </div>
  </div>
  <div id="child4" data-attribute="parent">
    <div id="grandchild2" data-attribute="child">
      <div id="grandchild3" data-attribute="parent">
        <div id="item2" data-attribute="child">
          <div id="sub1" data-attribute="child">
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

If the current element I'm performing query selection on is sub1, how do I find the last ancestor with data-attribute="parent"? In this case, the expected result should be parent2.

I know closest() will return the first match which would be grandchild3, but is there like a selector to find the final ancestor? Querying by id is not option, since my id's are dynamically created.

---

## link

https://stackoverflow.com/questions/58126606/how-to-traverse-dom-to-find-the-last-ancestor-with-specific-attribute-in-javascr/58126950#58126950