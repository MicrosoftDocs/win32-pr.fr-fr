---
title: Catégorisation des proxys et des stubs DCOM
description: Catégorisation des proxys et des stubs DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685cd1318856b9e305246cfebc2cebb3a7874e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509065"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a><span data-ttu-id="8ffcd-103">Catégorisation des proxys et des stubs DCOM</span><span class="sxs-lookup"><span data-stu-id="8ffcd-103">Categorizing DCOM Proxies and Stubs</span></span>

<span data-ttu-id="8ffcd-104">DCOM marshale les références aux objets en construisant des OBJREFs qui contiennent des CLSID.</span><span class="sxs-lookup"><span data-stu-id="8ffcd-104">DCOM marshals references to objects by constructing OBJREFs that contain CLSIDs.</span></span> <span data-ttu-id="8ffcd-105">Ces CLSID sont vulnérables aux attaques de sécurité, car les dll arbitraires peuvent être chargées pendant le marshaling.</span><span class="sxs-lookup"><span data-stu-id="8ffcd-105">These CLSIDs are vulnerable to security attacks because arbitrary DLLs can be loaded during marshaling.</span></span> <span data-ttu-id="8ffcd-106">Toutefois, l' \_ indicateur EOAC no \_ Custom \_ Marshal peut être spécifié lors de l’appel de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (consultez [**\_ \_ fonctionnalités d’authentification Eole**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span><span class="sxs-lookup"><span data-stu-id="8ffcd-106">However, the EOAC\_NO\_CUSTOM\_MARSHAL flag can be specified when calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (see [**EOLE\_AUTHENTICATION\_CAPABILITIES**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span></span> <span data-ttu-id="8ffcd-107">La définition de cet indicateur permet de protéger la sécurité du serveur lors de l’utilisation de DCOM, car cela réduit le risque d’exécution de dll arbitraires.</span><span class="sxs-lookup"><span data-stu-id="8ffcd-107">Setting this flag helps protect server security when using DCOM because it reduces the chances of executing arbitrary DLLs.</span></span> <span data-ttu-id="8ffcd-108">Lorsque cet indicateur est défini, le serveur autorise le marshaling des CLSID uniquement qui sont implémentés dans ole32.dll, comadmin.dll, comsvcs.dll ou es.dll, ou qui implémentent l’ID de \_ catégorie de marshaleur CATID.</span><span class="sxs-lookup"><span data-stu-id="8ffcd-108">When this flag is set, the server allows the marshaling only of CLSIDs that are implemented in ole32.dll, comadmin.dll, comsvcs.dll, or es.dll, or that implement the CATID\_MARSHALER category ID.</span></span>

<span data-ttu-id="8ffcd-109">\_Le marshaleur CATID est un GUID de catégorie de composant qui peut être associé à un CLSID qui est en cours de marshaling personnalisé.</span><span class="sxs-lookup"><span data-stu-id="8ffcd-109">CATID\_MARSHALER is a component category GUID that can be associated with a CLSID that is being custom marshaled.</span></span> <span data-ttu-id="8ffcd-110">Les interfaces en cours de marshaling personnalisé avec ce CLSID sont autorisées quand le EOAC \_ aucun \_ \_ Marshal personnalisé n’est défini via [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="8ffcd-110">The interfaces being custom marshaled with this CLSID are allowed when the EOAC\_NO\_CUSTOM\_MARSHAL is set via [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ffcd-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ffcd-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ffcd-112">Catégories de composant</span><span class="sxs-lookup"><span data-stu-id="8ffcd-112">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 