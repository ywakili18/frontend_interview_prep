# What is an event delegation?

      const parent = document.querySelector('#parent')

      parent.addEventListener('click', e => {
        if (e.target.id === 'child'){
          console.log('this works!')
        }
      })

This is the same if you were to select all child nodes using a queryselector all due to event bubbling/propagation.
