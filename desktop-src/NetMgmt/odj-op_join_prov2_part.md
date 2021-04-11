---
title: OP_JOINPROV2_PART
description: Définition du OP_JOINPROV2_PART IDL
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104102524"
---
# <a name="op_joinprov2_part-structure"></a><span data-ttu-id="4a4ef-103">Structure OP_JOINPROV2_PART</span><span class="sxs-lookup"><span data-stu-id="4a4ef-103">OP_JOINPROV2_PART structure</span></span>

<span data-ttu-id="4a4ef-104">Contient des informations supplémentaires utilisées pour la configuration d’un client joint à un domaine.</span><span class="sxs-lookup"><span data-stu-id="4a4ef-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a4ef-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a><span data-ttu-id="4a4ef-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4a4ef-106">Members</span></span>

### <a name="dwflags"></a><span data-ttu-id="4a4ef-107">dwFlags</span><span class="sxs-lookup"><span data-stu-id="4a4ef-107">dwFlags</span></span>

<span data-ttu-id="4a4ef-108">Doit être défini sur zéro ou sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a4ef-108">Must be set to either zero or one of the following values:</span></span>

|<span data-ttu-id="4a4ef-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a4ef-109">Value</span></span>|<span data-ttu-id="4a4ef-110">Signification</span><span class="sxs-lookup"><span data-stu-id="4a4ef-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="4a4ef-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="4a4ef-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span></span>|<span data-ttu-id="4a4ef-112">Le site spécifié dans lpSiteName doit être considéré comme le site permanent pour le client.</span><span class="sxs-lookup"><span data-stu-id="4a4ef-112">The site specified in lpSiteName MUST be considered the permanent site for the client.</span></span>|

### <a name="lpnetbiosname"></a><span data-ttu-id="4a4ef-113">lpNetbiosName</span><span class="sxs-lookup"><span data-stu-id="4a4ef-113">lpNetbiosName</span></span>

<span data-ttu-id="4a4ef-114">Contient le nom NetBIOS du compte d’ordinateur au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="4a4ef-114">Contains the Netbios name of the machine account in Unicode format.</span></span>

### <a name="lpsitename"></a><span data-ttu-id="4a4ef-115">lpSiteName</span><span class="sxs-lookup"><span data-stu-id="4a4ef-115">lpSiteName</span></span>

<span data-ttu-id="4a4ef-116">Contient le nom du site Active Directory que le client doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="4a4ef-116">Contains the name of the Active Directory site that the client should use.</span></span>

### <a name="lpprimarydnsdomain"></a><span data-ttu-id="4a4ef-117">lpPrimaryDNSDomain</span><span class="sxs-lookup"><span data-stu-id="4a4ef-117">lpPrimaryDNSDomain</span></span>

<span data-ttu-id="4a4ef-118">Contient le nom de domaine DNS principal que le client doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="4a4ef-118">Contains the primary DNS domain name that the client should use.</span></span>

### <a name="dwreserved"></a><span data-ttu-id="4a4ef-119">dwReserved</span><span class="sxs-lookup"><span data-stu-id="4a4ef-119">dwReserved</span></span>

<span data-ttu-id="4a4ef-120">Réservé pour une utilisation ultérieure et doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="4a4ef-120">Reserved for future use and must be set to 0.</span></span>

### <a name="lpreserved"></a><span data-ttu-id="4a4ef-121">lpReserved</span><span class="sxs-lookup"><span data-stu-id="4a4ef-121">lpReserved</span></span>

<span data-ttu-id="4a4ef-122">Réservé pour une utilisation ultérieure et doit avoir la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="4a4ef-122">Reserved for future use and must be set to NULL.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a4ef-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a4ef-123">See also</span></span>

[<span data-ttu-id="4a4ef-124">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="4a4ef-124">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
