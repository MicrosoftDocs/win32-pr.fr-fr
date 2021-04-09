---
description: Spécifie les attributs d’une signature Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: Structure SIGNER_ATTR_AUTHCODE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953146"
---
# <a name="signer_attr_authcode-structure"></a><span data-ttu-id="794da-103">\_Structure facteurs attr de signataire \_</span><span class="sxs-lookup"><span data-stu-id="794da-103">SIGNER\_ATTR\_AUTHCODE structure</span></span>

<span data-ttu-id="794da-104">La structure **\_ \_ facteurs attr du signataire** spécifie des attributs pour une signature [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="794da-104">The **SIGNER\_ATTR\_AUTHCODE** structure specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span>

> [!Note]  
> <span data-ttu-id="794da-105">Cette structure n’est définie dans aucun fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="794da-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="794da-106">Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="794da-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="794da-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="794da-107">Syntax</span></span>


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a><span data-ttu-id="794da-108">Membres</span><span class="sxs-lookup"><span data-stu-id="794da-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="794da-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="794da-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="794da-110">Taille, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="794da-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="794da-111">**fCommercial**</span><span class="sxs-lookup"><span data-stu-id="794da-111">**fCommercial**</span></span>
</dt> <dd>

<span data-ttu-id="794da-112">**True** pour signer le sujet en tant que serveur de publication commercial ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="794da-112">**TRUE** to sign the subject as a commercial publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="794da-113">**fIndividual**</span><span class="sxs-lookup"><span data-stu-id="794da-113">**fIndividual**</span></span>
</dt> <dd>

<span data-ttu-id="794da-114">**True** pour signer le sujet en tant qu’éditeur individuel ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="794da-114">**TRUE** to sign the subject as an individual publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="794da-115">**pwszName**</span><span class="sxs-lookup"><span data-stu-id="794da-115">**pwszName**</span></span>
</dt> <dd>

<span data-ttu-id="794da-116">Nom complet du fichier lors du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="794da-116">The display name of the file upon download.</span></span>

</dd> <dt>

<span data-ttu-id="794da-117">**pwszInfo**</span><span class="sxs-lookup"><span data-stu-id="794da-117">**pwszInfo**</span></span>
</dt> <dd>

<span data-ttu-id="794da-118">Nom complet de l’URL du fichier lors du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="794da-118">The display name of the URL of the file upon download.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="794da-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="794da-119">Requirements</span></span>



| <span data-ttu-id="794da-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="794da-120">Requirement</span></span> | <span data-ttu-id="794da-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="794da-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="794da-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="794da-122">Minimum supported client</span></span><br/> | <span data-ttu-id="794da-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="794da-123">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="794da-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="794da-124">Minimum supported server</span></span><br/> | <span data-ttu-id="794da-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="794da-125">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="794da-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="794da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="794da-127">**informations de \_ signature du signataire \_**</span><span class="sxs-lookup"><span data-stu-id="794da-127">**SIGNER\_SIGNATURE\_INFO**</span></span>](signer-signature-info.md)
</dt> </dl>

 

 
