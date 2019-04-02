# Título

Esta es una prueba de formato, *itálica* y **negritas**, _itálica 2_ y __negritas 2__, __*Itálicas y Negritas*__, ~Tachado~, 

## Subtítulo

### Subtítulo

#### Subtítulo

##### Subtítulo

###### Subtítulo

####### Falso subtítulo

# Imágenes

C++ Logo (externo)

![C++ Logo](https://upload.wikimedia.org/wikipedia/commons/1/18/ISO_C%2B%2B_Logo.svg)

Avatar (interna)

![Phoenix](/ikkiplata.jpg)

# Links

[AWS Cloud](https://aws.amazon.com/es/)

[Test File](/HelloWorld.txt)

# Code Snippers

Python Code:

``` python
def sucesor(n):
  return n + 1
```

Java Code:

``` java
package test.avisphoenix.hellojpa.utils.paginator;

import java.util.ArrayList;
import java.util.List;

import org.springframework.data.domain.Page;

public class PageRender<T> {
	
	private String url;
	private Page<T> page;
	
	private int totalPages;
	private int itemsPerPage;
	private int currentPage;
	
	private List<PageItem> paginas;
	
	
	public PageRender(String url, Page<T> page) {
		super();
		this.url = url;
		this.page = page;
		this.paginas = new ArrayList<PageItem>();
		
		itemsPerPage = page.getSize();
		totalPages = page.getTotalPages();
		currentPage = page.getNumber() + 1;
		
		int desde, hasta;
		if (totalPages <= itemsPerPage ) {
			desde = 1;
			hasta = totalPages;
		} else {
			if (currentPage <= itemsPerPage/2) { 
				desde = 1;
				hasta = itemsPerPage;
			} else if (currentPage >= totalPages - itemsPerPage/2) {
				desde = totalPages + itemsPerPage + 1;
				hasta = itemsPerPage;
			} else {
				desde = currentPage - itemsPerPage/2;
				hasta = itemsPerPage;
			}
		}
		
		for ( int i=0; i < hasta; i++) {
			paginas.add(new PageItem(desde + i, currentPage == desde + i));
		}
	}
}
```

# Listas

Numeradas:

1. One
  1. One One
  2. Two One
2. Two
3. Three

Balas:

* One
* Two
  * One Two
  * Two Two
* Three
  - One Three
  - Two Three
  
# Emojis

[Lista de Emojis](https://www.webfx.com/tools/emoji-cheat-sheet/)


:bowtie: :wink: :weary: :no_mouth: :neutral_face:

# Tablas

Cabecera 1 | Cabecera 2
---------- | ----------
Elemento 1 | Elemento 2
Elemento 3 | Elemento 4
Elemento 5 | Elemento 6

# CheckList

-[x] Tarea 1
-[ ] Tarea 2
-[ ] Tarea 3
-[x] Tarea 4
