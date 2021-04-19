---
description: Spécifie un fichier à signer.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: Structure SIGNER_FILE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524444"
---
# <a name="signer_file_info-structure"></a><span data-ttu-id="b97a9-103">Structure d' \_ informations du fichier signataire \_</span><span class="sxs-lookup"><span data-stu-id="b97a9-103">SIGNER\_FILE\_INFO structure</span></span>

<span data-ttu-id="b97a9-104">La structure d' **\_ \_ informations du fichier de signataire** spécifie un fichier à signer.</span><span class="sxs-lookup"><span data-stu-id="b97a9-104">The **SIGNER\_FILE\_INFO** structure specifies a file to sign.</span></span>

> [!Note]  
> <span data-ttu-id="b97a9-105">Cette structure n’est définie dans aucun fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="b97a9-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="b97a9-106">Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b97a9-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b97a9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b97a9-107">Syntax</span></span>


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a><span data-ttu-id="b97a9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b97a9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b97a9-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="b97a9-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="b97a9-110">Taille, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="b97a9-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="b97a9-111">**pwszFileName**</span><span class="sxs-lookup"><span data-stu-id="b97a9-111">**pwszFileName**</span></span>
</dt> <dd>

<span data-ttu-id="b97a9-112">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du fichier à signer.</span><span class="sxs-lookup"><span data-stu-id="b97a9-112">A pointer to a null-terminated string that contains the name of the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="b97a9-113">**hFile**</span><span class="sxs-lookup"><span data-stu-id="b97a9-113">**hFile**</span></span>
</dt> <dd>

<span data-ttu-id="b97a9-114">Handle ouvert du fichier spécifié par le membre **pwszFileName** .</span><span class="sxs-lookup"><span data-stu-id="b97a9-114">An open handle to the file specified by the **pwszFileName** member.</span></span> <span data-ttu-id="b97a9-115">Si ce membre contient un handle valide, ce handle est utilisé pour accéder au fichier.</span><span class="sxs-lookup"><span data-stu-id="b97a9-115">If this member contains a valid handle, this handle is used to access the file.</span></span> <span data-ttu-id="b97a9-116">Ce membre peut avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="b97a9-116">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b97a9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b97a9-117">Requirements</span></span>



| <span data-ttu-id="b97a9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b97a9-118">Requirement</span></span> | <span data-ttu-id="b97a9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97a9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b97a9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b97a9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b97a9-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b97a9-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b97a9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b97a9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b97a9-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b97a9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b97a9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b97a9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b97a9-125">**informations d' \_ objet du signataire \_**</span><span class="sxs-lookup"><span data-stu-id="b97a9-125">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 




