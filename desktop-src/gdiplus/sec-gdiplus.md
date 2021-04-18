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
# <a name="security-considerations-gdi"></a><span data-ttu-id="1edfc-103">Considérations relatives à la sécurité : GDI+</span><span class="sxs-lookup"><span data-stu-id="1edfc-103">Security Considerations: GDI+</span></span>

<span data-ttu-id="1edfc-104">Cette rubrique fournit des informations sur les considérations de sécurité liées à la programmation avec Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="1edfc-104">This topic provides information about security considerations related to programming with Windows GDI+.</span></span> <span data-ttu-id="1edfc-105">Cette rubrique ne fournit pas tout ce que vous devez savoir sur les problèmes de sécurité. Utilisez-la plutôt comme point de départ et référence pour ce domaine technologique.</span><span class="sxs-lookup"><span data-stu-id="1edfc-105">This topic doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="1edfc-106">Vérification de la réussite des constructeurs</span><span class="sxs-lookup"><span data-stu-id="1edfc-106">Verifying the Success of Constructors</span></span>](#verifying-the-success-of-constructors)
-   [<span data-ttu-id="1edfc-107">Allouer des tampons</span><span class="sxs-lookup"><span data-stu-id="1edfc-107">Allocating Buffers</span></span>](#allocating-buffers)
-   [<span data-ttu-id="1edfc-108">Vérification des erreurs</span><span class="sxs-lookup"><span data-stu-id="1edfc-108">Error Checking</span></span>](#error-checking)
-   [<span data-ttu-id="1edfc-109">Synchronisation des threads</span><span class="sxs-lookup"><span data-stu-id="1edfc-109">Thread Synchronization</span></span>](#thread-synchronization)
-   [<span data-ttu-id="1edfc-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1edfc-110">Related topics</span></span>](#related-topics)

## <a name="verifying-the-success-of-constructors"></a><span data-ttu-id="1edfc-111">Vérification de la réussite des constructeurs</span><span class="sxs-lookup"><span data-stu-id="1edfc-111">Verifying the Success of Constructors</span></span>

<span data-ttu-id="1edfc-112">La plupart des classes GDI+ fournissent une méthode [**image :: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) que vous pouvez appeler pour déterminer si les méthodes appelées sur un objet réussissent.</span><span class="sxs-lookup"><span data-stu-id="1edfc-112">Many of the GDI+ classes provide a [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method that you can call to determine whether methods invoked on an object are successful.</span></span> <span data-ttu-id="1edfc-113">Vous pouvez également appeler **image :: GetLastStatus** pour déterminer si un constructeur réussit.</span><span class="sxs-lookup"><span data-stu-id="1edfc-113">You can also call **Image::GetLastStatus** to determine whether a constructor is successful.</span></span>

<span data-ttu-id="1edfc-114">L’exemple suivant montre comment construire un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et appeler la méthode [**image :: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) pour déterminer si le constructeur a réussi.</span><span class="sxs-lookup"><span data-stu-id="1edfc-114">The following example shows how to construct an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and call the [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method to determine whether the constructor was successful.</span></span> <span data-ttu-id="1edfc-115">Les valeurs **OK** et **InvalidParameter** sont des éléments de l’énumération d' [**État**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) .</span><span class="sxs-lookup"><span data-stu-id="1edfc-115">The values **Ok** and **InvalidParameter** are elements of the [**Status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) enumeration.</span></span>


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



## <a name="allocating-buffers"></a><span data-ttu-id="1edfc-116">Allouer des tampons</span><span class="sxs-lookup"><span data-stu-id="1edfc-116">Allocating Buffers</span></span>

<span data-ttu-id="1edfc-117">Plusieurs méthodes GDI+ retournent des données numériques ou caractères dans une mémoire tampon allouée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="1edfc-117">Several GDI+ methods return numeric or character data in a buffer that is allocated by the caller.</span></span> <span data-ttu-id="1edfc-118">Pour chacune de ces méthodes, il existe une méthode auxiliaire qui donne la taille de la mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="1edfc-118">For each of those methods, there is a companion method that gives the size of the required buffer.</span></span> <span data-ttu-id="1edfc-119">Par exemple, la méthode [**GraphicsPath :: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) retourne un tableau d’objets [**point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="1edfc-119">For example, the [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) method returns an array of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="1edfc-120">Avant d’appeler **GraphicsPath :: GetPathPoints**, vous devez allouer une mémoire tampon suffisamment grande pour contenir ce tableau.</span><span class="sxs-lookup"><span data-stu-id="1edfc-120">Before you call **GraphicsPath::GetPathPoints**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="1edfc-121">Vous pouvez déterminer la taille de la mémoire tampon requise en appelant la méthode [**GraphicsPath :: GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) d’un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="1edfc-121">You can determine the size of the required buffer by calling the [**GraphicsPath::GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span>

<span data-ttu-id="1edfc-122">L’exemple suivant montre comment déterminer le nombre de points dans un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , allouer une mémoire tampon suffisamment grande pour contenir ce nombre de points, puis appeler [**GraphicsPath :: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) pour remplir la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1edfc-122">The following example shows how to determine the number of points in a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object, allocate a buffer large enough to hold that many points, and then call [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) to fill the buffer.</span></span> <span data-ttu-id="1edfc-123">Avant que le code appelle **GraphicsPath :: GetPathPoints**, il vérifie que l’allocation de mémoire tampon s’est correctement déroulée en s’assurant que le pointeur de la mémoire tampon n’est pas **null**.</span><span class="sxs-lookup"><span data-stu-id="1edfc-123">Before the code calls **GraphicsPath::GetPathPoints**, it verifies that the buffer allocation was successful by making sure that the buffer pointer is not **NULL**.</span></span>


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



<span data-ttu-id="1edfc-124">L’exemple précédent utilise l’opérateur New pour allouer une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1edfc-124">The previous example uses the new operator to allocate a buffer.</span></span> <span data-ttu-id="1edfc-125">Le nouvel opérateur était pratique, car la mémoire tampon a été remplie avec un nombre connu d’objets [**point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="1edfc-125">The new operator was convenient because the buffer was filled with a known number of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="1edfc-126">Dans certains cas, GDI+ écrit plus de mémoire tampon qu’un tableau d’objets GDI+.</span><span class="sxs-lookup"><span data-stu-id="1edfc-126">In some cases, GDI+ writes more into buffer than an array of GDI+ objects.</span></span> <span data-ttu-id="1edfc-127">Parfois, une mémoire tampon est remplie avec un tableau d’objets GDI+, ainsi que des données supplémentaires pointées par les membres de ces objets.</span><span class="sxs-lookup"><span data-stu-id="1edfc-127">Sometimes a buffer is filled with an array of GDI+ objects along with additional data that is pointed to by members of those objects.</span></span> <span data-ttu-id="1edfc-128">Par exemple, la méthode [**image :: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) retourne un tableau d’objets [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , un pour chaque élément de propriété (métadonnées) stocké dans l’image.</span><span class="sxs-lookup"><span data-stu-id="1edfc-128">For example, the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method returns an array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects, one for each property item (piece of metadata) stored in the image.</span></span> <span data-ttu-id="1edfc-129">Mais **image :: GetAllPropertyItems** retourne plus que le tableau d’objets **PropertyItem** ; Il ajoute le tableau avec des données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1edfc-129">But **Image::GetAllPropertyItems** returns more than just the array of **PropertyItem** objects; it appends the array with additional data.</span></span>

<span data-ttu-id="1edfc-130">Avant d’appeler [**image :: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), vous devez allouer une mémoire tampon suffisamment grande pour contenir le tableau d’objets [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) avec les données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1edfc-130">Before you call [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), you must allocate a buffer large enough to hold the array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects along with the additional data.</span></span> <span data-ttu-id="1edfc-131">Vous pouvez appeler la méthode [**image :: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) d’un objet image pour déterminer la taille totale de la mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="1edfc-131">You can call the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method of an Image object to determine the total size of the required buffer.</span></span>

<span data-ttu-id="1edfc-132">L’exemple suivant montre comment créer un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et appeler ultérieurement la méthode [**image :: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) de cet objet **image** pour récupérer tous les éléments de propriété (métadonnées) stockés dans l’image.</span><span class="sxs-lookup"><span data-stu-id="1edfc-132">The following example shows how to create an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and later call the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method of that **Image** object to retrieve all the property items (metadata) stored in the image.</span></span> <span data-ttu-id="1edfc-133">Le code alloue une mémoire tampon en fonction d’une valeur de taille retournée par la méthode [**image :: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) .</span><span class="sxs-lookup"><span data-stu-id="1edfc-133">The code allocates a buffer based on a size value returned by the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method.</span></span> <span data-ttu-id="1edfc-134">**Image :: GetPropertySize** retourne également une valeur de nombre qui donne le nombre d’éléments de propriété dans l’image.</span><span class="sxs-lookup"><span data-stu-id="1edfc-134">**Image::GetPropertySize** also returns a count value that gives the number of property items in the image.</span></span> <span data-ttu-id="1edfc-135">Notez que le code ne calcule pas la taille de la mémoire tampon sous la forme `count*sizeof(PropertyItem)` .</span><span class="sxs-lookup"><span data-stu-id="1edfc-135">Notice that the code does not calculate the buffer size as `count*sizeof(PropertyItem)`.</span></span> <span data-ttu-id="1edfc-136">Une mémoire tampon calculée de cette façon est trop petite.</span><span class="sxs-lookup"><span data-stu-id="1edfc-136">A buffer calculated that way would be too small.</span></span>


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



## <a name="error-checking"></a><span data-ttu-id="1edfc-137">Vérification des erreurs</span><span class="sxs-lookup"><span data-stu-id="1edfc-137">Error Checking</span></span>

<span data-ttu-id="1edfc-138">La plupart des exemples de code dans la documentation GDI+ n’affichent pas la vérification des erreurs.</span><span class="sxs-lookup"><span data-stu-id="1edfc-138">Most of the code examples in the GDI+ documentation do not show error checking.</span></span> <span data-ttu-id="1edfc-139">La vérification complète des erreurs rend un exemple de code plus long et peut obscurcir le point représenté par l’exemple.</span><span class="sxs-lookup"><span data-stu-id="1edfc-139">Complete error checking makes a code example much longer and can obscure the point being illustrated by the example.</span></span> <span data-ttu-id="1edfc-140">Vous ne devez pas coller des exemples de la documentation directement dans le code de production ; au lieu de cela, vous devez améliorer les exemples en ajoutant votre propre vérification des erreurs.</span><span class="sxs-lookup"><span data-stu-id="1edfc-140">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

<span data-ttu-id="1edfc-141">L’exemple suivant montre une façon d’implémenter la vérification des erreurs avec GDI+.</span><span class="sxs-lookup"><span data-stu-id="1edfc-141">The following example shows one way of implementing error checking with GDI+.</span></span> <span data-ttu-id="1edfc-142">Chaque fois qu’un objet GDI+ est construit, le code vérifie si le constructeur a réussi.</span><span class="sxs-lookup"><span data-stu-id="1edfc-142">Each time a GDI+ object is constructed, the code checks to see whether the constructor was successful.</span></span> <span data-ttu-id="1edfc-143">Cette vérification est particulièrement importante pour le constructeur d' [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , qui s’appuie sur la lecture d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="1edfc-143">That check is especially important for the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) constructor, which relies on reading a file.</span></span> <span data-ttu-id="1edfc-144">Si les quatre objets GDI+ ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **image** et [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) sont construits avec succès, le code appelle des méthodes sur ces objets.</span><span class="sxs-lookup"><span data-stu-id="1edfc-144">If all four of the GDI+ objects ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image**, and [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) are constructed successfully, the code calls methods on those objects.</span></span> <span data-ttu-id="1edfc-145">La réussite de chaque appel de méthode est vérifiée et, en cas d’échec, les appels de méthode restants sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="1edfc-145">Each method call is checked for success, and in the event of failure, the remaining method calls are skipped.</span></span>


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



## <a name="thread-synchronization"></a><span data-ttu-id="1edfc-146">Synchronisation des threads</span><span class="sxs-lookup"><span data-stu-id="1edfc-146">Thread Synchronization</span></span>

<span data-ttu-id="1edfc-147">Il est possible que plusieurs threads aient accès à un seul objet GDI+.</span><span class="sxs-lookup"><span data-stu-id="1edfc-147">It is possible for more than one thread to have access to a single GDI+ object.</span></span> <span data-ttu-id="1edfc-148">Toutefois, GDI+ ne fournit pas de mécanisme de synchronisation automatique.</span><span class="sxs-lookup"><span data-stu-id="1edfc-148">However, GDI+ does not provide any automatic synchronization mechanism.</span></span> <span data-ttu-id="1edfc-149">Par conséquent, si deux threads de votre application ont un pointeur vers le même objet GDI+, il vous incombe de synchroniser l’accès à cet objet.</span><span class="sxs-lookup"><span data-stu-id="1edfc-149">So if two threads in your application have a pointer to the same GDI+ object, it is your responsibility to synchronize access to that object.</span></span>

<span data-ttu-id="1edfc-150">Certaines méthodes GDI+ retournent **ObjectBusy** si un thread tente d’appeler une méthode alors qu’un autre thread exécute une méthode sur le même objet.</span><span class="sxs-lookup"><span data-stu-id="1edfc-150">Some GDI+ methods return **ObjectBusy** if a thread attempts to call a method while another thread is executing a method on the same object.</span></span> <span data-ttu-id="1edfc-151">N’essayez pas de synchroniser l’accès à un objet en fonction de la valeur de retour **ObjectBusy** .</span><span class="sxs-lookup"><span data-stu-id="1edfc-151">Do not try to synchronize access to an object based on the **ObjectBusy** return value.</span></span> <span data-ttu-id="1edfc-152">Au lieu de cela, chaque fois que vous accédez à un membre ou appelez une méthode de l’objet, placez l’appel à l’intérieur d’une section critique ou utilisez une autre technique de synchronisation standard.</span><span class="sxs-lookup"><span data-stu-id="1edfc-152">Instead, each time you access a member or call a method of the object, place the call inside a critical section, or use some other standard synchronization technique.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1edfc-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1edfc-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1edfc-154">Centre de développement Sécurité sur le site MSDN</span><span class="sxs-lookup"><span data-stu-id="1edfc-154">MSDN Security Developer Center</span></span>](https://msdn.microsoft.com/security/)
</dt> <dt>

<span data-ttu-id="1edfc-155">[Ressources de How-To de sécurité](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="1edfc-155">[Security How-To Resources](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span></span>
</dt> <dt>

[<span data-ttu-id="1edfc-156">Security Center TechNet</span><span class="sxs-lookup"><span data-stu-id="1edfc-156">TechNet Security Center</span></span>](https://technet.microsoft.com/security/)
</dt> </dl>

 

 
