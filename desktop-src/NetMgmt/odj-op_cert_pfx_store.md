---
title: OP_CERT_PFX_STORE
description: Définition du OP_CERT_PFX_STORE IDL
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: b07d0b8e5572763cc42fe2f5b19a4dde2cfe2157
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "106509284"
---
# <a name="op_cert_pfx_store-structure"></a><span data-ttu-id="4c104-103">Structure OP_CERT_PFX_STORE</span><span class="sxs-lookup"><span data-stu-id="4c104-103">OP_CERT_PFX_STORE structure</span></span>

<span data-ttu-id="4c104-104">Contient une structure PFX sérialisée.</span><span class="sxs-lookup"><span data-stu-id="4c104-104">Contains a serialized PFX structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c104-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c104-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a><span data-ttu-id="4c104-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4c104-106">Members</span></span>

### <a name="ptemplatename"></a><span data-ttu-id="4c104-107">pTemplateName</span><span class="sxs-lookup"><span data-stu-id="4c104-107">pTemplateName</span></span>

<span data-ttu-id="4c104-108">Doit être défini sur le nom du modèle de certificat utilisé pour créer le certificat.</span><span class="sxs-lookup"><span data-stu-id="4c104-108">Must be set to the name of the certificate template used to create the certificate.</span></span>

### <a name="ulprivatekeyexportpolicy"></a><span data-ttu-id="4c104-109">ulPrivateKeyExportPolicy</span><span class="sxs-lookup"><span data-stu-id="4c104-109">ulPrivateKeyExportPolicy</span></span>

<span data-ttu-id="4c104-110">Contient une valeur de l’énumération [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) .</span><span class="sxs-lookup"><span data-stu-id="4c104-110">Contains one value from the [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) enumeration.</span></span>

### <a name="ppolicyserverurl"></a><span data-ttu-id="4c104-111">pPolicyServerUrl</span><span class="sxs-lookup"><span data-stu-id="4c104-111">pPolicyServerUrl</span></span>

<span data-ttu-id="4c104-112">Doit être défini sur l’URL du serveur de stratégie.</span><span class="sxs-lookup"><span data-stu-id="4c104-112">Must be set the URL of the policy server.</span></span>

### <a name="ulpolicyserverurlflags"></a><span data-ttu-id="4c104-113">ulPolicyServerUrlFlags</span><span class="sxs-lookup"><span data-stu-id="4c104-113">ulPolicyServerUrlFlags</span></span>

<span data-ttu-id="4c104-114">Contient une valeur de l’énumération [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) .</span><span class="sxs-lookup"><span data-stu-id="4c104-114">Contains one value from the [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) enumeration.</span></span>

### <a name="ppolicyserverid"></a><span data-ttu-id="4c104-115">pPolicyServerId</span><span class="sxs-lookup"><span data-stu-id="4c104-115">pPolicyServerId</span></span>

<span data-ttu-id="4c104-116">Contient une chaîne qui identifie de façon unique le serveur de stratégie</span><span class="sxs-lookup"><span data-stu-id="4c104-116">Contains a string that uniquely identifies the policy server</span></span>

### <a name="cbpfx"></a><span data-ttu-id="4c104-117">cbPfx</span><span class="sxs-lookup"><span data-stu-id="4c104-117">cbPfx</span></span>

<span data-ttu-id="4c104-118">Contient la taille de pPfx en octets.</span><span class="sxs-lookup"><span data-stu-id="4c104-118">Contains the size of pPfx in bytes.</span></span>

### <a name="ppfx"></a><span data-ttu-id="4c104-119">pPfx</span><span class="sxs-lookup"><span data-stu-id="4c104-119">pPfx</span></span>

<span data-ttu-id="4c104-120">Contient une structure PFX sérialisée (voir [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span><span class="sxs-lookup"><span data-stu-id="4c104-120">Contains a serialized PFX structure (see [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span></span>

## <a name="see-also"></a><span data-ttu-id="4c104-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c104-121">See also</span></span>

[<span data-ttu-id="4c104-122">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="4c104-122">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
