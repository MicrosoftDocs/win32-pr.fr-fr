---
description: La propriété DVDAdm. BookmarkOnStop définit ou récupère une valeur qui indique à l’objet MSWebDVD s’il faut enregistrer automatiquement un signet de l’emplacement et des paramètres actuels lorsque l’utilisateur clique sur le bouton arrêter.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Propriété BookmarkOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109538"
---
# <a name="bookmarkonstop-property"></a><span data-ttu-id="3576c-103">Propriété BookmarkOnStop</span><span class="sxs-lookup"><span data-stu-id="3576c-103">BookmarkOnStop Property</span></span>

<span data-ttu-id="3576c-104">La `DVDAdm.BookmarkOnStop` propriété définit ou récupère une valeur qui indique à l’objet mswebdvd s’il faut enregistrer automatiquement un signet de l’emplacement et des paramètres actuels lorsque l’utilisateur clique sur le bouton **arrêter** .</span><span class="sxs-lookup"><span data-stu-id="3576c-104">The `DVDAdm.BookmarkOnStop` property sets or retrieves a value that tells the MSWebDVD object whether to automatically save a bookmark of the current location and settings when the user clicks the **Stop** button.</span></span>

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a><span data-ttu-id="3576c-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3576c-105">Return Value</span></span>

<span data-ttu-id="3576c-106">Retourne une valeur booléenne indiquant si l’objet MSDVDAdm enregistre un signet de tous les paramètres DVD, y compris la position sur le disque, le niveau parental et le pays/région parent.</span><span class="sxs-lookup"><span data-stu-id="3576c-106">Returns a Boolean value indicating whether the MSDVDAdm object will save a bookmark of all DVD settings including position on disc, parental level and parental country/region.</span></span>

## <a name="remarks"></a><span data-ttu-id="3576c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3576c-107">Remarks</span></span>

<span data-ttu-id="3576c-108">Cette propriété est en lecture/écriture et sa valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="3576c-108">This property is read/write with a default value of false.</span></span>

<span data-ttu-id="3576c-109">Les signets sont valides uniquement pour un ordinateur particulier.</span><span class="sxs-lookup"><span data-stu-id="3576c-109">Bookmarks are valid only for a particular machine.</span></span> <span data-ttu-id="3576c-110">Un utilisateur ne peut pas enregistrer un signet, puis l’envoyer à un autre utilisateur pour le lire sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3576c-110">A user cannot save a bookmark and then send it to someone else to read on a different machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="3576c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3576c-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3576c-112">**BookmarkOnClose**</span><span class="sxs-lookup"><span data-stu-id="3576c-112">**BookmarkOnClose**</span></span>](bookmarkonclose-property.md)
</dt> <dt>

[<span data-ttu-id="3576c-113">Objet MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="3576c-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



