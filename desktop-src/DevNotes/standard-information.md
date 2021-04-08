---
description: Contient l’attribut d’informations standard. Cet attribut est présent dans chaque enregistrement de fichier de base et doit être résident.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: Structure STANDARD_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033573"
---
# <a name="standard_information-structure"></a><span data-ttu-id="f506e-104">\_Structure d’informations standard</span><span class="sxs-lookup"><span data-stu-id="f506e-104">STANDARD\_INFORMATION structure</span></span>

<span data-ttu-id="f506e-105">\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="f506e-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="f506e-106">Contient l’attribut d’informations standard.</span><span class="sxs-lookup"><span data-stu-id="f506e-106">Contains the standard information attribute.</span></span> <span data-ttu-id="f506e-107">Cet attribut est présent dans chaque enregistrement de fichier de base et doit être résident.</span><span class="sxs-lookup"><span data-stu-id="f506e-107">This attribute is present in every base file record and must be resident.</span></span>

## <a name="syntax"></a><span data-ttu-id="f506e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f506e-108">Syntax</span></span>


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="f506e-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f506e-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="f506e-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f506e-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f506e-111">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f506e-111">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f506e-112">**OwnerId**</span><span class="sxs-lookup"><span data-stu-id="f506e-112">**OwnerId**</span></span>
</dt> <dd>

<span data-ttu-id="f506e-113">Identificateur du propriétaire du fichier, à partir de l’index de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f506e-113">The identifier of the file owner, from the security index.</span></span>

</dd> <dt>

<span data-ttu-id="f506e-114">**SecurityId**</span><span class="sxs-lookup"><span data-stu-id="f506e-114">**SecurityId**</span></span>
</dt> <dd>

<span data-ttu-id="f506e-115">Identificateur de sécurité du fichier.</span><span class="sxs-lookup"><span data-stu-id="f506e-115">The security identifier for the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f506e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f506e-116">Remarks</span></span>

<span data-ttu-id="f506e-117">Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="f506e-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="f506e-118">Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="f506e-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="f506e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f506e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f506e-120">Table de fichiers maîtres</span><span class="sxs-lookup"><span data-stu-id="f506e-120">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
