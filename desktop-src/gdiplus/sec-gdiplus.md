---
description: Cette rubrique fournit des informations sur les considérations de sécurité liées à la programmation avec Windows GDI+.
ms.assetid: 411e16e4-ad8f-4567-8964-564f08283ba5
title: 'Considérations relatives à la sécurité : GDI+'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d8c9d50393708e58651566ee90adcb4339cb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991305"
---
# <a name="security-considerations-gdi"></a>Considérations relatives à la sécurité : GDI+

Cette rubrique fournit des informations sur les considérations de sécurité liées à la programmation avec Windows GDI+. Cette rubrique ne fournit pas tout ce que vous devez savoir sur les problèmes de sécurité. Utilisez-la plutôt comme point de départ et référence pour ce domaine technologique.

-   [Vérification de la réussite des constructeurs](#verifying-the-success-of-constructors)
-   [Allouer des tampons](#allocating-buffers)
-   [Vérification des erreurs](#error-checking)
-   [Synchronisation des threads](#thread-synchronization)
-   [Rubriques connexes](#related-topics)

## <a name="verifying-the-success-of-constructors"></a>Vérification de la réussite des constructeurs

La plupart des classes GDI+ fournissent une méthode [**image :: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) que vous pouvez appeler pour déterminer si les méthodes appelées sur un objet réussissent. Vous pouvez également appeler **image :: GetLastStatus** pour déterminer si un constructeur réussit.

L’exemple suivant montre comment construire un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et appeler la méthode [**image :: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) pour déterminer si le constructeur a réussi. Les valeurs **OK** et **InvalidParameter** sont des éléments de l’énumération d' [**État**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) .


```C++
Image myImage(L"Climber.jpg");
Status st = myImage.GetLastStatus();

if(Ok == st)
   // The constructor was successful. Use myImage.
else if(InvalidParameter == st)
   // The constructor failed because of an invalid parameter.
else
   // Compare st to other elements of the Status 
   // enumeration or do general error processing.
```



## <a name="allocating-buffers"></a>Allouer des tampons

Plusieurs méthodes GDI+ retournent des données numériques ou caractères dans une mémoire tampon allouée par l’appelant. Pour chacune de ces méthodes, il existe une méthode auxiliaire qui donne la taille de la mémoire tampon requise. Par exemple, la méthode [**GraphicsPath :: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) retourne un tableau d’objets [**point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . Avant d’appeler **GraphicsPath :: GetPathPoints**, vous devez allouer une mémoire tampon suffisamment grande pour contenir ce tableau. Vous pouvez déterminer la taille de la mémoire tampon requise en appelant la méthode [**GraphicsPath :: GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) d’un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .

L’exemple suivant montre comment déterminer le nombre de points dans un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , allouer une mémoire tampon suffisamment grande pour contenir ce nombre de points, puis appeler [**GraphicsPath :: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) pour remplir la mémoire tampon. Avant que le code appelle **GraphicsPath :: GetPathPoints**, il vérifie que l’allocation de mémoire tampon s’est correctement déroulée en s’assurant que le pointeur de la mémoire tampon n’est pas **null**.


```C++
GraphicsPath path;
path.AddEllipse(10, 10, 200, 100);

INT count = path.GetPointCount();          // get the size
Point* pointArray = new Point[count];      // allocate the buffer

if(pointArray)  // Check for successful allocation.
{
   path.GetPathPoints(pointArray, count);  // get the data
   ...                                     // use pointArray
   delete[] pointArray;                    // release the buffer
   pointArray = NULL;
}
```



L’exemple précédent utilise l’opérateur New pour allouer une mémoire tampon. Le nouvel opérateur était pratique, car la mémoire tampon a été remplie avec un nombre connu d’objets [**point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . Dans certains cas, GDI+ écrit plus de mémoire tampon qu’un tableau d’objets GDI+. Parfois, une mémoire tampon est remplie avec un tableau d’objets GDI+, ainsi que des données supplémentaires pointées par les membres de ces objets. Par exemple, la méthode [**image :: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) retourne un tableau d’objets [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , un pour chaque élément de propriété (métadonnées) stocké dans l’image. Mais **image :: GetAllPropertyItems** retourne plus que le tableau d’objets **PropertyItem** ; Il ajoute le tableau avec des données supplémentaires.

Avant d’appeler [**image :: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), vous devez allouer une mémoire tampon suffisamment grande pour contenir le tableau d’objets [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) avec les données supplémentaires. Vous pouvez appeler la méthode [**image :: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) d’un objet image pour déterminer la taille totale de la mémoire tampon requise.

L’exemple suivant montre comment créer un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et appeler ultérieurement la méthode [**image :: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) de cet objet **image** pour récupérer tous les éléments de propriété (métadonnées) stockés dans l’image. Le code alloue une mémoire tampon en fonction d’une valeur de taille retournée par la méthode [**image :: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) . **Image :: GetPropertySize** retourne également une valeur de nombre qui donne le nombre d’éléments de propriété dans l’image. Notez que le code ne calcule pas la taille de la mémoire tampon sous la forme `count*sizeof(PropertyItem)` . Une mémoire tampon calculée de cette façon est trop petite.


```C++
UINT count = 0;
UINT size = 0;
Image myImage(L"FakePhoto.jpg");
myImage.GetPropertySize(&size, &count);

// GetAllPropertyItems returns an array of PropertyItem objects
// along with additional data. Allocate a buffer large enough to 
// receive the array and the additional data.
PropertyItem* propBuffer =(PropertyItem*)malloc(size);

if(propBuffer)
{
   myImage.GetAllPropertyItems(size, count, propBuffer);
   ...
   free(propBuffer);
   propBuffer = NULL;
}
```



## <a name="error-checking"></a>Vérification des erreurs

La plupart des exemples de code dans la documentation GDI+ n’affichent pas la vérification des erreurs. La vérification complète des erreurs rend un exemple de code plus long et peut obscurcir le point représenté par l’exemple. Vous ne devez pas coller des exemples de la documentation directement dans le code de production ; au lieu de cela, vous devez améliorer les exemples en ajoutant votre propre vérification des erreurs.

L’exemple suivant montre une façon d’implémenter la vérification des erreurs avec GDI+. Chaque fois qu’un objet GDI+ est construit, le code vérifie si le constructeur a réussi. Cette vérification est particulièrement importante pour le constructeur d' [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , qui s’appuie sur la lecture d’un fichier. Si les quatre objets GDI+ ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **image** et [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) sont construits avec succès, le code appelle des méthodes sur ces objets. La réussite de chaque appel de méthode est vérifiée et, en cas d’échec, les appels de méthode restants sont ignorés.


```C++
Status GdipExample(HDC hdc)
{
   Status status = GenericError;
   INT count = 0;
   Point* points = NULL;

   Graphics graphics(hdc);
   status = graphics.GetLastStatus();
   if(Ok != status)
      return status;

   GraphicsPath path;
   status = path.GetLastStatus();
   if(Ok != status)
      return status;

   Image image(L"MyTexture.bmp");
   status = image.GetLastStatus();
   if(Ok != status)
      return status;

   TextureBrush brush(&image);
   status = brush.GetLastStatus();
   if(Ok != status)
      return status;

   status = path.AddEllipse(10, 10, 200, 100);

   if(Ok == status)
   {
      status = path.AddBezier(40, 130, 200, 130, 200, 200, 60, 200);
   }
  
   if(Ok == status)
   {
      count = path.GetPointCount();
      status = path.GetLastStatus();
   }

   if(Ok == status)
   {
      points = new Point[count];

      if(NULL == points)
         status = OutOfMemory;
   }

   if(Ok == status)
   {
      status = path.GetPathPoints(points, count);  
   }
  
   if(Ok == status)
   {
      status = graphics.FillPath(&brush, &path);
   }
   
   if(Ok == status)
   {
      for(int j = 0; j < count; ++j)
      {
         status = graphics.FillEllipse(
         &brush, points[j].X - 5, points[j].Y - 5, 10, 10);
      }
   }

   if(points)
   {
      delete[] points;
      points = NULL;
   }

   return status;
}
```



## <a name="thread-synchronization"></a>Synchronisation des threads

Il est possible que plusieurs threads aient accès à un seul objet GDI+. Toutefois, GDI+ ne fournit pas de mécanisme de synchronisation automatique. Par conséquent, si deux threads de votre application ont un pointeur vers le même objet GDI+, il vous incombe de synchroniser l’accès à cet objet.

Certaines méthodes GDI+ retournent **ObjectBusy** si un thread tente d’appeler une méthode alors qu’un autre thread exécute une méthode sur le même objet. N’essayez pas de synchroniser l’accès à un objet en fonction de la valeur de retour **ObjectBusy** . Au lieu de cela, chaque fois que vous accédez à un membre ou appelez une méthode de l’objet, placez l’appel à l’intérieur d’une section critique ou utilisez une autre technique de synchronisation standard.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Centre de développement Sécurité sur le site MSDN](https://msdn.microsoft.com/security/)
</dt> <dt>

[Ressources de How-To de sécurité](/previous-versions/msp-n-p/ff650055(v=pandp.10))
</dt> <dt>

[Security Center TechNet](https://technet.microsoft.com/security/)
</dt> </dl>

 

 
