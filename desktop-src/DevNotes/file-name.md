---
description: Représente un attribut de nom de fichier. Un fichier a un attribut de nom de fichier pour chaque répertoire dans lequel il est entré.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: Structure FILE_NAME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033581"
---
# <a name="file_name-structure"></a><span data-ttu-id="77795-104">Structure de nom de fichier \_</span><span class="sxs-lookup"><span data-stu-id="77795-104">FILE\_NAME structure</span></span>

<span data-ttu-id="77795-105">\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="77795-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="77795-106">Représente un attribut de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="77795-106">Represents a file name attribute.</span></span> <span data-ttu-id="77795-107">Un fichier a un attribut de nom de fichier pour chaque répertoire dans lequel il est entré.</span><span class="sxs-lookup"><span data-stu-id="77795-107">A file has one file name attribute for every directory it is entered into.</span></span>

## <a name="syntax"></a><span data-ttu-id="77795-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77795-108">Syntax</span></span>


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a><span data-ttu-id="77795-109">Membres</span><span class="sxs-lookup"><span data-stu-id="77795-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="77795-110">**ParentDirectory**</span><span class="sxs-lookup"><span data-stu-id="77795-110">**ParentDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="77795-111">Référence de fichier au répertoire qui indexe ce nom.</span><span class="sxs-lookup"><span data-stu-id="77795-111">A file reference to the directory that indexes to this name.</span></span> <span data-ttu-id="77795-112">Consultez [**\_ \_ référence de segment MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="77795-112">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="77795-113">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="77795-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="77795-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="77795-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="77795-115">**FileNameLength**</span><span class="sxs-lookup"><span data-stu-id="77795-115">**FileNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="77795-116">Longueur du nom de fichier, en caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="77795-116">The length of the file name, in Unicode characters.</span></span>

</dd> <dt>

<span data-ttu-id="77795-117">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="77795-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="77795-118">Indicateurs de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="77795-118">The file name flags.</span></span>

<dl> <dt>

<span data-ttu-id="77795-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**Fichier \_ NOM \_ NTFS** (0x01)</span><span class="sxs-lookup"><span data-stu-id="77795-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**FILE\_NAME\_NTFS** (0x01)</span></span>
</dt> <dt>

<span data-ttu-id="77795-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**Fichier \_ NOM \_ dos** (0x02)</span><span class="sxs-lookup"><span data-stu-id="77795-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**FILE\_NAME\_DOS** (0x02)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="77795-121">**FileName**</span><span class="sxs-lookup"><span data-stu-id="77795-121">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="77795-122">Premier caractère du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="77795-122">The first character of the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77795-123">Notes</span><span class="sxs-lookup"><span data-stu-id="77795-123">Remarks</span></span>

<span data-ttu-id="77795-124">Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="77795-124">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="77795-125">Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="77795-125">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="77795-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77795-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77795-127">Table de fichiers maîtres</span><span class="sxs-lookup"><span data-stu-id="77795-127">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
