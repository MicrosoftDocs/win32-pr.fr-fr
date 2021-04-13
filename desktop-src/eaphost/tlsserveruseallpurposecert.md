---
title: TlsServerUseAllPurposeCert
description: La clé de Registre TlsServerUseAllPurposeCert détermine si les certificats polyvalents sont utilisés pour l’authentification EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104313813"
---
# <a name="tlsserveruseallpurposecert"></a><span data-ttu-id="39fcf-103">TlsServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="39fcf-103">TlsServerUseAllPurposeCert</span></span>

<span data-ttu-id="39fcf-104">La clé de Registre TlsServerUseAllPurposeCert détermine si les certificats polyvalents sont utilisés pour l’authentification EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="39fcf-104">The TlsServerUseAllPurposeCert registry key determines if all-purpose certificates are used for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="39fcf-105">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="39fcf-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="39fcf-106">Notes</span><span class="sxs-lookup"><span data-stu-id="39fcf-106">Remarks</span></span>

<span data-ttu-id="39fcf-107">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="39fcf-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="39fcf-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="39fcf-108">Value</span></span>        | <span data-ttu-id="39fcf-109">Description</span><span class="sxs-lookup"><span data-stu-id="39fcf-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39fcf-110">1</span><span class="sxs-lookup"><span data-stu-id="39fcf-110">1</span></span>            | <span data-ttu-id="39fcf-111">Les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="39fcf-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="39fcf-112">Autres valeurs</span><span class="sxs-lookup"><span data-stu-id="39fcf-112">Other values</span></span> | <span data-ttu-id="39fcf-113">Les certificats à usage général dans le magasin de certificats du client ou du serveur ne sont pas sélectionnés pour l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="39fcf-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="39fcf-114">Si cette valeur de Registre n’est pas présente, les certificats à usage général dans le magasin de certificats du client ou du serveur sont sélectionnés pour l’authentification EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="39fcf-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39fcf-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39fcf-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39fcf-116">Paramètres du Registre EAPHost</span><span class="sxs-lookup"><span data-stu-id="39fcf-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




