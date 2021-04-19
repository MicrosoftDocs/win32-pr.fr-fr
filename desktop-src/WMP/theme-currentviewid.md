---
title: THÈME. currentViewID
description: L’attribut currentViewID spécifie ou récupère la vue actuellement affichée.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- THEMe. currentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545491"
---
# <a name="themecurrentviewid"></a><span data-ttu-id="3adee-104">THÈME. currentViewID</span><span class="sxs-lookup"><span data-stu-id="3adee-104">THEME.currentViewID</span></span>

<span data-ttu-id="3adee-105">L’attribut **currentViewID** spécifie ou récupère la **vue** actuellement affichée.</span><span class="sxs-lookup"><span data-stu-id="3adee-105">The **currentViewID** attribute specifies or retrieves the currently displayed **VIEW**.</span></span>

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a><span data-ttu-id="3adee-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="3adee-106">Possible Values</span></span>

<span data-ttu-id="3adee-107">Cet attribut est une **chaîne** en lecture/écriture spécifiant l' **ID** de la **vue** actuelle.</span><span class="sxs-lookup"><span data-stu-id="3adee-107">This attribute is a read/write **String** specifying the **id** of the current **VIEW**.</span></span> <span data-ttu-id="3adee-108">Il n'a aucune valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3adee-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3adee-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3adee-109">Remarks</span></span>

<span data-ttu-id="3adee-110">La spécification de **currentViewID** ferme automatiquement la **currentView** existante (vers laquelle pointe l’attribut **View** global) et ouvre la **vue** spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3adee-110">Specifying **currentViewID** automatically closes the existing **currentView** (pointed to by the **view** global attribute) and opens the specified **VIEW**.</span></span>

## <a name="examples"></a><span data-ttu-id="3adee-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="3adee-111">Examples</span></span>


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="3adee-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3adee-112">Requirements</span></span>



| <span data-ttu-id="3adee-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3adee-113">Requirement</span></span> | <span data-ttu-id="3adee-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3adee-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3adee-115">Version</span><span class="sxs-lookup"><span data-stu-id="3adee-115">Version</span></span><br/> | <span data-ttu-id="3adee-116">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="3adee-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3adee-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3adee-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3adee-118">**Élément THEMe**</span><span class="sxs-lookup"><span data-stu-id="3adee-118">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





