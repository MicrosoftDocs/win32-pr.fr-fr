---
title: Lecture des valeurs d’attribut
description: Lecture des valeurs d’attribut
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Lecteur Windows Media, attributs des éléments multimédias
- Modèle objet du lecteur Windows Media, attributs des éléments multimédias
- modèle objet, attributs pour les éléments multimédias
- Windows Media Player Mobile, attributs pour les éléments multimédias
- Contrôle ActiveX du lecteur Windows Media, attributs des éléments multimédias
- Contrôle ActiveX Windows Media Player Mobile, attributs des éléments multimédias
- Contrôle ActiveX, attributs pour les éléments multimédias
- Bibliothèque du lecteur Windows Media, attributs pour les éléments multimédias
- bibliothèque, attributs pour les éléments multimédias
- attributs, lire des valeurs
- lecture des valeurs d’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512270"
---
# <a name="reading-attribute-values"></a><span data-ttu-id="b0b0d-114">Lecture des valeurs d’attribut</span><span class="sxs-lookup"><span data-stu-id="b0b0d-114">Reading Attribute Values</span></span>

<span data-ttu-id="b0b0d-115">Les attributs que vous pouvez trouver dans la bibliothèque et dans les fichiers Windows Media ont des noms prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-115">The attributes you can find in the library and in Windows Media files have predefined names.</span></span> <span data-ttu-id="b0b0d-116">Vous pouvez écrire du code qui récupère la valeur d’un attribut en passant le nom de cet attribut au *média*. **getItemInfo** ou *Media*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-116">You can write code that retrieves the value of one attribute by passing the name of that attribute to *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="b0b0d-117">Vous pouvez également écrire du code qui récupère les valeurs de tous les attributs d’un fichier ou d’un élément.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-117">You can also write code that retrieves the values of all of the attributes in a file or item.</span></span>

<span data-ttu-id="b0b0d-118">L’exemple C# suivant récupère la valeur de l’attribut **title** et l’affiche dans une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-118">The following C# example retrieves the value of the **Title** attribute and displays it in a message box.</span></span> <span data-ttu-id="b0b0d-119">Dans cet exemple, l’objet **Player** a été défini en tant que AxWMPLib. AxWindowsMediaPlayer Player.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-119">In this example, the **Player** object was defined as axWMPLib.AxWindowsMediaPlayer Player.</span></span>


```C++
IWMPMedia media;
string strAttribValue = "";

// Initialize the media object
media = Player.currentMedia;

// Retrieve the object's Title attribute
strAttribValue = media.getItemInfo("Title");

// Display the title
if (strAttribValue != "")
{
    MessageBox.Show("Current title: " + strAttribValue);
}

```



<span data-ttu-id="b0b0d-120">Dans l’appel à **getItemInfoByType**, le deuxième paramètre est une chaîne qui spécifie la langue.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-120">In the call to **getItemInfoByType**, the second parameter is a string that specifies the language.</span></span> <span data-ttu-id="b0b0d-121">Si vous transmettez une chaîne vide comme indiqué dans cet exemple, la méthode récupère la valeur dans la langue par défaut.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-121">If you pass an empty string as shown in this example, the method retrieves the value in the default language.</span></span> <span data-ttu-id="b0b0d-122">Pour plus d’informations sur le troisième paramètre, consultez [attributs avec plusieurs valeurs](attributes-with-multiple-values.md).</span><span class="sxs-lookup"><span data-stu-id="b0b0d-122">For information about the third parameter, see [Attributes with Multiple Values](attributes-with-multiple-values.md).</span></span>

<span data-ttu-id="b0b0d-123">L’exemple C# suivant récupère les valeurs d’un attribut donné dans l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-123">The following C# example retrieves the values for a given attribute in the current media item.</span></span> <span data-ttu-id="b0b0d-124">Elle retourne ces valeurs sous la forme d’une chaîne délimitée par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-124">It returns these values as a semicolon-delimited string.</span></span> <span data-ttu-id="b0b0d-125">Notez que pour les attributs représentés sous forme d’objets, tels que **WM/paroles \_ synchronisés**, **WM/Picture** et **WM/UserWebURL**, la fonction retourne une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-125">Note that for attributes represented as objects, such as **WM/Lyrics\_Synchronised**, **WM/Picture**, and **WM/UserWebURL**, the function returns an empty string.</span></span>


```C++
private string getAttributeValues(string strAttrName, IWMPMedia3 media)
{
    string strAttrValue = "";
    int iAttrCount = 0;

    if (media != null)
    {
        // Retrieve the count of values for this attribute
        iAttrCount = media.getAttributeCountByType(strAttrName, "");

        // Retrieve the values
        for (int i = 0; i < iAttrCount; i++)
        {
            strAttrValue += media.getItemInfoByType(strAttrName, "", i);
            strAttrValue += ";";
        }
    }

    // Return the resulting string
    return strAttrValue;
}

```



<span data-ttu-id="b0b0d-126">Le troisième argument passé à la méthode **getItemInfoByType** est l’index d’un attribut particulier dans un ensemble d’attributs portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-126">The third argument passed to the **getItemInfoByType** method is the index of a particular attribute in a set of attributes with the same name.</span></span>

<span data-ttu-id="b0b0d-127">Vous pouvez utiliser du code similaire pour récupérer des attributs qui ont des noms uniques.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-127">You can use similar code to retrieve attributes that have unique names.</span></span> <span data-ttu-id="b0b0d-128">Dans ce cas, **getAttributeCountByType** retourne 1.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-128">In those cases, **getAttributeCountByType** returns 1.</span></span> <span data-ttu-id="b0b0d-129">Dans l’exemple ci-dessus, l’appel à **getItemInfoByType** ne s’exécute qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="b0b0d-129">In the example shown earlier, the call to **getItemInfoByType** would execute only once.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0b0d-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0b0d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0b0d-131">**Modification des valeurs d’attribut**</span><span class="sxs-lookup"><span data-stu-id="b0b0d-131">**Changing Attribute Values**</span></span>](changing-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="b0b0d-132">**Attributs d’élément multimédia**</span><span class="sxs-lookup"><span data-stu-id="b0b0d-132">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="b0b0d-133">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="b0b0d-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="b0b0d-134">**Lecture des valeurs d’attribut à partir d’un CD ou d’un DVD**</span><span class="sxs-lookup"><span data-stu-id="b0b0d-134">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




