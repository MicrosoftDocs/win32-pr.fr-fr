---
description: Définition des propriétés personnalisées.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Définition des propriétés personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd91ee4d4e657ce0d6c01330d85e8df4ef57a36d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519909"
---
# <a name="defining-custom-properties"></a><span data-ttu-id="72123-103">Définition des propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="72123-103">Defining Custom Properties</span></span>

<span data-ttu-id="72123-104">**Définition des propriétés personnalisées**.</span><span class="sxs-lookup"><span data-stu-id="72123-104">**Defining Custom Properties**.</span></span>

<span data-ttu-id="72123-105">Si le minipilote d’acquisition d’images Windows (WIA) est nécessaire pour définir des propriétés personnalisées, la \_ \_ propriété DEVPROP privée WIA doit être utilisée pour les propriétés d’élément racine personnalisées, et la \_ \_ propriété ITEMPROP privée WIA "doit être utilisée pour d’autres propriétés d’élément.</span><span class="sxs-lookup"><span data-stu-id="72123-105">If it is necessary for the Windows Image Acquisition (WIA) minidriver to define custom properties, the WIA\_PRIVATE\_DEVPROP property should be used for custom root item properties, and the WIA\_PRIVATE\_ITEMPROP" property should be used for other item properties.</span></span> <span data-ttu-id="72123-106">Ces constantes sont définies dans *wiadef. h*.</span><span class="sxs-lookup"><span data-stu-id="72123-106">These constants are defined in *wiadef.h*.</span></span>

<span data-ttu-id="72123-107">L’exemple de code suivant montre des définitions pour trois propriétés d’élément racine.</span><span class="sxs-lookup"><span data-stu-id="72123-107">The following example code shows definitions for three root item properties.</span></span> <span data-ttu-id="72123-108">L’ID de propriété de la première propriété d’élément racine personnalisée \_ , \_ prop source personnalisée \_ 1, est défini en termes \_ de \_ DEVPROP privés WIA.</span><span class="sxs-lookup"><span data-stu-id="72123-108">The property ID for the first custom root item property, CUSTOM\_ROOT\_PROP\_1, is defined in terms of WIA\_PRIVATE\_DEVPROP.</span></span> <span data-ttu-id="72123-109">Les ID de propriété pour les propriétés d’élément racine supplémentaires sont définis en termes de \_ DEVPROP privée WIA \_ + 1, WIA \_ Private \_ DEVPROP + 2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="72123-109">Property IDs for additional root item properties are defined in terms of WIA\_PRIVATE\_DEVPROP + 1, WIA\_PRIVATE\_DEVPROP + 2, and so on.</span></span> <span data-ttu-id="72123-110">Le modèle peut être poursuivi si des propriétés d’élément racine personnalisées supplémentaires sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="72123-110">The pattern can be continued if additional custom root item properties are needed.</span></span>


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



<span data-ttu-id="72123-111">L’exemple suivant montre des définitions pour trois propriétés d’élément enfant personnalisées et ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="72123-111">The next example shows definitions for three custom child item properties and property IDs.</span></span> <span data-ttu-id="72123-112">L’ID de propriété de la première propriété d’élément enfant personnalisé \_ , \_ prop enfant personnalisée \_ 1, est défini en termes \_ de \_ ITEMPROP privés WIA.</span><span class="sxs-lookup"><span data-stu-id="72123-112">The property ID for the first custom child item property, CUSTOM\_CHILD\_PROP\_1, is defined in terms of WIA\_PRIVATE\_ITEMPROP.</span></span> <span data-ttu-id="72123-113">Les ID de propriété pour les propriétés d’élément enfant supplémentaires sont définis en termes de \_ ITEMPROP privé WIA \_ + 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="72123-113">Property IDs for additional child item properties are defined in terms of WIA\_PRIVATE\_ITEMPROP + 1, and so on.</span></span> <span data-ttu-id="72123-114">Comme précédemment, le modèle peut être poursuivi si davantage de propriétés d’élément enfant personnalisées sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="72123-114">As before, the pattern can be continued if more of these custom child item properties are needed.</span></span>


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



<span data-ttu-id="72123-115">Les propriétés WIA personnalisées doivent avoir des noms de propriétés personnalisés associés aux ID de propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="72123-115">Custom WIA properties must have custom property names that are associated with the custom property IDs.</span></span> <span data-ttu-id="72123-116">L’exemple de code suivant montre des définitions pour trois noms de propriété d’élément racine personnalisés.</span><span class="sxs-lookup"><span data-stu-id="72123-116">The following example code shows definitions for three custom root item property names.</span></span> <span data-ttu-id="72123-117">(Ces noms de propriétés sont utilisés avec les ID de propriétés personnalisées qui ont été créés dans un exemple précédent, où le nom de la propriété personnalisée contenu dans CUSTOM \_ \_La prop racine \_ 1 \_ Str est associée à l’ID de propriété de l’élément racine personnalisé prop de la \_ racine personnalisée \_ \_ 1.)</span><span class="sxs-lookup"><span data-stu-id="72123-117">(These property names are used with the custom property IDs that were created in a previous example, where the custom property name contained in CUSTOM\_ROOT\_PROP\_1\_STR is associated with the custom root item property ID CUSTOM\_ROOT\_PROP\_1.)</span></span>


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> <span data-ttu-id="72123-118">Les noms de propriété WIA ne sont *pas* localisés dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="72123-118">WIA property names are *not* localized in multiple languages.</span></span> <span data-ttu-id="72123-119">Cela est dû au fait que les propriétés WIA peuvent être lues par les applications à l’aide de l’ID de propriété ou du nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="72123-119">This is because WIA properties can be read by applications using the property ID or the property name.</span></span> <span data-ttu-id="72123-120">Si le nom est utilisé, il doit s’agir d’une constante, tout comme l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="72123-120">If the name is used, it must be a constant, just as the property ID is.</span></span>

 

 

 



