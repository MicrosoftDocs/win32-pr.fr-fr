---
title: PeapServerAcceptAllPurposeCert
description: La clé de Registre PeapServerAcceptAllPurposeCert détermine si les certificats à usage général sont acceptés pour l’authentification PEAP.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106543044"
---
# <a name="peapserveracceptallpurposecert"></a><span data-ttu-id="865cb-103">PeapServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="865cb-103">PeapServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="865cb-104">La clé de Registre PeapServerAcceptAllPurposeCert détermine si les certificats à usage général sont acceptés pour l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="865cb-104">The PeapServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="865cb-105">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="865cb-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="865cb-106">Notes</span><span class="sxs-lookup"><span data-stu-id="865cb-106">Remarks</span></span>

<span data-ttu-id="865cb-107">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="865cb-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="865cb-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="865cb-108">Value</span></span>        | <span data-ttu-id="865cb-109">Description</span><span class="sxs-lookup"><span data-stu-id="865cb-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="865cb-110">1</span><span class="sxs-lookup"><span data-stu-id="865cb-110">1</span></span>            | <span data-ttu-id="865cb-111">Le serveur et le client acceptent les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="865cb-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="865cb-112">Autres valeurs</span><span class="sxs-lookup"><span data-stu-id="865cb-112">Other values</span></span> | <span data-ttu-id="865cb-113">Le serveur et le client n’acceptent pas les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="865cb-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="865cb-114">Si cette valeur de Registre n’est pas présente, le serveur et le client acceptent les certificats à usage général envoyés par l’autre partie pour l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="865cb-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="865cb-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="865cb-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="865cb-116">Paramètres du Registre EAPHost</span><span class="sxs-lookup"><span data-stu-id="865cb-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




