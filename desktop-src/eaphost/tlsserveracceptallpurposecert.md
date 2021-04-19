---
title: TlsServerAcceptAllPurposeCert
description: La clé de Registre TlsServerAcceptAllPurposeCert détermine si les certificats polyvalents sont acceptés pour l’authentification EAP-TLS.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106512709"
---
# <a name="tlsserveracceptallpurposecert"></a><span data-ttu-id="81e8b-103">TlsServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="81e8b-103">TlsServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="81e8b-104">La clé de Registre TlsServerAcceptAllPurposeCert détermine si les certificats polyvalents sont acceptés pour l’authentification EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="81e8b-104">The TlsServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="81e8b-105">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="81e8b-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="81e8b-106">Notes</span><span class="sxs-lookup"><span data-stu-id="81e8b-106">Remarks</span></span>

<span data-ttu-id="81e8b-107">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="81e8b-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="81e8b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="81e8b-108">Value</span></span>        | <span data-ttu-id="81e8b-109">Description</span><span class="sxs-lookup"><span data-stu-id="81e8b-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e8b-110">1</span><span class="sxs-lookup"><span data-stu-id="81e8b-110">1</span></span>            | <span data-ttu-id="81e8b-111">Le serveur et le client acceptent les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="81e8b-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="81e8b-112">Autres valeurs</span><span class="sxs-lookup"><span data-stu-id="81e8b-112">Other values</span></span> | <span data-ttu-id="81e8b-113">Le serveur et le client n’acceptent pas les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="81e8b-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="81e8b-114">Si cette valeur de Registre n’est pas présente, le serveur et le client acceptent les certificats à usage général envoyés par l’autre partie pour l’authentification EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="81e8b-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81e8b-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81e8b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81e8b-116">Paramètres du Registre EAPHost</span><span class="sxs-lookup"><span data-stu-id="81e8b-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




