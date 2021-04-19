---
description: Spécifie un objet à signer.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: Structure SIGNER_SUBJECT_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520522"
---
# <a name="signer_subject_info-structure"></a><span data-ttu-id="adf25-103">Structure des informations de l’objet du signataire \_ \_</span><span class="sxs-lookup"><span data-stu-id="adf25-103">SIGNER\_SUBJECT\_INFO structure</span></span>

<span data-ttu-id="adf25-104">La structure d' **\_ \_ informations** sur l’objet du signataire spécifie un objet à signer.</span><span class="sxs-lookup"><span data-stu-id="adf25-104">The **SIGNER\_SUBJECT\_INFO** structure specifies a subject to sign.</span></span>

> [!Note]  
> <span data-ttu-id="adf25-105">Cette structure n’est définie dans aucun fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="adf25-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="adf25-106">Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="adf25-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="adf25-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adf25-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a><span data-ttu-id="adf25-108">Membres</span><span class="sxs-lookup"><span data-stu-id="adf25-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="adf25-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="adf25-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="adf25-110">Taille, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="adf25-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="adf25-111">**pdwIndex**</span><span class="sxs-lookup"><span data-stu-id="adf25-111">**pdwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="adf25-112">Ce membre est réservé.</span><span class="sxs-lookup"><span data-stu-id="adf25-112">This member is reserved.</span></span> <span data-ttu-id="adf25-113">Elle doit être définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="adf25-113">It must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="adf25-114">**dwSubjectChoice**</span><span class="sxs-lookup"><span data-stu-id="adf25-114">**dwSubjectChoice**</span></span>
</dt> <dd>

<span data-ttu-id="adf25-115">Spécifie si l’objet est un fichier ou un [*objet BLOB*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="adf25-115">Specifies whether the subject is a file or a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="adf25-116">Ce membre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="adf25-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="adf25-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="adf25-117">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="adf25-118">Signification</span><span class="sxs-lookup"><span data-stu-id="adf25-118">Meaning</span></span>                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <span data-ttu-id="adf25-119"><dt>**Signataire \_ OBJET \_ BLOB**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="adf25-119"><dt>**SIGNER\_SUBJECT\_BLOB**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="adf25-120">L’objet est un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="adf25-120">The subject is a BLOB.</span></span><br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <span data-ttu-id="adf25-121"><dt>**Signataire \_ \_Fichier objet**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="adf25-121"><dt>**SIGNER\_SUBJECT\_FILE**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="adf25-122">L’objet est un fichier.</span><span class="sxs-lookup"><span data-stu-id="adf25-122">The subject is a file.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="adf25-123">**pSignerFileInfo**</span><span class="sxs-lookup"><span data-stu-id="adf25-123">**pSignerFileInfo**</span></span>
</dt> <dd>

<span data-ttu-id="adf25-124">Pointeur vers une structure d' [**\_ \_ informations de fichier du signataire**](signer-file-info.md) qui spécifie le fichier à signer.</span><span class="sxs-lookup"><span data-stu-id="adf25-124">A pointer to a [**SIGNER\_FILE\_INFO**](signer-file-info.md) structure that specifies the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="adf25-125">**pSignerBlobInfo**</span><span class="sxs-lookup"><span data-stu-id="adf25-125">**pSignerBlobInfo**</span></span>
</dt> <dd>

<span data-ttu-id="adf25-126">Pointeur vers une structure d' [**\_ \_ informations d’objet blob de signataire**](signer-blob-info.md) qui spécifie l’objet blob à signer.</span><span class="sxs-lookup"><span data-stu-id="adf25-126">A pointer to a [**SIGNER\_BLOB\_INFO**](signer-blob-info.md) structure that specifies the BLOB to sign.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="adf25-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adf25-127">Requirements</span></span>



| <span data-ttu-id="adf25-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adf25-128">Requirement</span></span> | <span data-ttu-id="adf25-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="adf25-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="adf25-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adf25-130">Minimum supported client</span></span><br/> | <span data-ttu-id="adf25-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adf25-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="adf25-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adf25-132">Minimum supported server</span></span><br/> | <span data-ttu-id="adf25-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adf25-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="adf25-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adf25-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf25-135">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="adf25-135">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="adf25-136">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="adf25-136">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
