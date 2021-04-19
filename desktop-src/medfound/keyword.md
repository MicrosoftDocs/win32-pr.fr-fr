---
description: Spécifie un mot clé pour un fournisseur MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: Keyword, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11632a257e7d51378ddb816124e51548746a178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527243"
---
# <a name="keyword-element"></a><span data-ttu-id="13d9e-103">Keyword, élément</span><span class="sxs-lookup"><span data-stu-id="13d9e-103">keyword element</span></span>

<span data-ttu-id="13d9e-104">Spécifie un mot clé pour un fournisseur [MFTrace](mftrace.md) .</span><span class="sxs-lookup"><span data-stu-id="13d9e-104">Specifies a key word for an [MFTrace](mftrace.md) provider.</span></span>

## <a name="usage"></a><span data-ttu-id="13d9e-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="13d9e-105">Usage</span></span>

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a><span data-ttu-id="13d9e-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="13d9e-106">Attributes</span></span>



| <span data-ttu-id="13d9e-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="13d9e-107">Attribute</span></span>         | <span data-ttu-id="13d9e-108">Type</span><span class="sxs-lookup"><span data-stu-id="13d9e-108">Type</span></span>             | <span data-ttu-id="13d9e-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="13d9e-109">Required</span></span>       | <span data-ttu-id="13d9e-110">Description</span><span class="sxs-lookup"><span data-stu-id="13d9e-110">Description</span></span>                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="13d9e-111">**Identifiant**</span><span class="sxs-lookup"><span data-stu-id="13d9e-111">**ID**</span></span><br/> | <span data-ttu-id="13d9e-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="13d9e-112">CDATA</span></span><br/> | <span data-ttu-id="13d9e-113">Oui</span><span class="sxs-lookup"><span data-stu-id="13d9e-113">Yes</span></span><br/> | <span data-ttu-id="13d9e-114">Nom ou masque du mot clé</span><span class="sxs-lookup"><span data-stu-id="13d9e-114">The name or mask of the key word</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="13d9e-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="13d9e-115">Child elements</span></span>

<span data-ttu-id="13d9e-116">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="13d9e-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="13d9e-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="13d9e-117">Parent elements</span></span>



| <span data-ttu-id="13d9e-118">Élément</span><span class="sxs-lookup"><span data-stu-id="13d9e-118">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="13d9e-119">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="13d9e-119">**mfdetours**</span></span>](mfdetours.md)<br/> |
| [<span data-ttu-id="13d9e-120">**moteur**</span><span class="sxs-lookup"><span data-stu-id="13d9e-120">**provider**</span></span>](provider.md)<br/>   |



## <a name="remarks"></a><span data-ttu-id="13d9e-121">Notes</span><span class="sxs-lookup"><span data-stu-id="13d9e-121">Remarks</span></span>

<span data-ttu-id="13d9e-122">Pour l’élément [**mfdetours**](mfdetours.md) , les mots clés valides sont répertoriés dans la rubrique [MFTrace Keywords](mftrace-keywords.md).</span><span class="sxs-lookup"><span data-stu-id="13d9e-122">For the [**mfdetours**](mfdetours.md) element, the valid key words are listed in the topic [MFTrace Keywords](mftrace-keywords.md).</span></span>

<span data-ttu-id="13d9e-123">Pour l’élément [**Provider**](provider.md) , les mots clés dépendent du fournisseur d’événements.</span><span class="sxs-lookup"><span data-stu-id="13d9e-123">For the [**provider**](provider.md) element, the key words depend on the event provider.</span></span> <span data-ttu-id="13d9e-124">Vous pouvez utiliser l’utilitaire Wevtutil.exe pour répertorier les mots clés d’un fournisseur donné.</span><span class="sxs-lookup"><span data-stu-id="13d9e-124">You can use the Wevtutil.exe utility to list the key words for a given provider.</span></span>

## <a name="element-information"></a><span data-ttu-id="13d9e-125">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="13d9e-125">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="13d9e-126">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="13d9e-126">Can be empty</span></span> | <span data-ttu-id="13d9e-127">Oui</span><span class="sxs-lookup"><span data-stu-id="13d9e-127">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="13d9e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13d9e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d9e-129">Fichier de configuration MFTrace</span><span class="sxs-lookup"><span data-stu-id="13d9e-129">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="13d9e-130">Mots clés MFTrace</span><span class="sxs-lookup"><span data-stu-id="13d9e-130">MFTrace Keywords</span></span>](mftrace-keywords.md)
</dt> </dl>

 

 




