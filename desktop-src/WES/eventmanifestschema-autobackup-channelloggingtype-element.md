---
title: Élément de sauvegarde autoChannelLoggingType
description: Détermine s’il est impossible de créer un nouveau fichier journal lorsque le fichier journal actuel atteint sa taille maximale.
ms.assetid: 708c5d44-d20b-437a-a01f-6182b244c736
keywords:
- EventLog, élément d’élément de sauvegarde
topic_type:
- apiref
api_name:
- autoBackup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d69c1a1c43be9d2376d94f39b3158e167f7bd13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519082"
---
# <a name="autobackup-channelloggingtype-element"></a><span data-ttu-id="8ab82-104">Élément de sauvegarde autoChannelLoggingType</span><span class="sxs-lookup"><span data-stu-id="8ab82-104">autoBackup (ChannelLoggingType) Element</span></span>

<span data-ttu-id="8ab82-105">Détermine s’il est impossible de créer un nouveau fichier journal lorsque le fichier journal actuel atteint sa taille maximale.</span><span class="sxs-lookup"><span data-stu-id="8ab82-105">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span>

``` syntax
<xs:element name="autoBackup"
    type="boolean"
 />
```

<span data-ttu-id="8ab82-106">L’élément **Autobackup** est défini par le type complexe [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8ab82-106">The **autoBackup** element is defined by the [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ab82-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ab82-107">Requirements</span></span>



| <span data-ttu-id="8ab82-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ab82-108">Requirement</span></span> | <span data-ttu-id="8ab82-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ab82-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ab82-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ab82-110">Minimum supported client</span></span><br/> | <span data-ttu-id="8ab82-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ab82-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8ab82-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ab82-112">Minimum supported server</span></span><br/> | <span data-ttu-id="8ab82-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ab82-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ab82-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ab82-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ab82-115">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="8ab82-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="8ab82-116">**journalisation (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="8ab82-116">**logging (ChannelType)**</span></span>](eventmanifestschema-logging-channeltype-element.md)
</dt> </dl>

 

 





