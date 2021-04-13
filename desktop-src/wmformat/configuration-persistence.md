---
title: Persistance de la configuration
description: Persistance de la configuration
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Media Format SDK, persistance
- Windows Media Format SDK, persistance de configuration
- Format de systèmes avancés (ASF), persistance
- ASF (format des systèmes avancés), persistance
- Format de systèmes avancés (ASF), persistance de configuration
- ASF (format de systèmes avancés), persistance de configuration
- persistance de la configuration
- persistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381561"
---
# <a name="configuration-persistence"></a><span data-ttu-id="61278-111">Persistance de la configuration</span><span class="sxs-lookup"><span data-stu-id="61278-111">Configuration Persistence</span></span>

<span data-ttu-id="61278-112">Aucune des propriétés activées en écriture décrites dans cette documentation n’est enregistrée par le kit de développement logiciel (SDK) Windows Media.</span><span class="sxs-lookup"><span data-stu-id="61278-112">None of the write-enabled properties described in this documentation are saved by the Windows Media SDK.</span></span> <span data-ttu-id="61278-113">Chaque application qui utilise le kit de développement logiciel (SDK) doit fournir ses propres procédures de persistance en fonction des besoins et appeler la méthode Set appropriée sur chaque instance du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="61278-113">Each application that uses the SDK must provide its own persistence procedures as needed and invoke the appropriate set method upon each instance of the SDK.</span></span> <span data-ttu-id="61278-114">De cette façon, les modifications de configuration apportées par une application n’affectent pas une autre application.</span><span class="sxs-lookup"><span data-stu-id="61278-114">In this way, configuration changes made by one application do not affect another application.</span></span> <span data-ttu-id="61278-115">Par exemple, la modification du temps de mise en mémoire tampon dans un joueur n’affecte pas un autre lecteur.</span><span class="sxs-lookup"><span data-stu-id="61278-115">For example, changing the buffering time in one player does not affect another player.</span></span>

<span data-ttu-id="61278-116">La seule exception à cette règle concerne les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="61278-116">The one exception to this rule is for the credentials information.</span></span> <span data-ttu-id="61278-117">Si l’application indique, dans son retour de l’appel **AcquireCredentials** , que les informations d’ID d’utilisateur et de mot de passe doivent être persistantes, le kit de développement logiciel (SDK) enregistre ces informations.</span><span class="sxs-lookup"><span data-stu-id="61278-117">If the application indicates, in its return from the **AcquireCredentials** call, that the user ID and password information must be persisted, the SDK saves this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61278-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61278-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61278-119">**Implémentation des fonctionnalités réseau**</span><span class="sxs-lookup"><span data-stu-id="61278-119">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="61278-120">**Interface IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="61278-120">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




