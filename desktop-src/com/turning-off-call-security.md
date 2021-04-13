---
title: Désactivation de la sécurité de l’appel
description: La sécurité de l’appel détermine si un client a l’autorisation d’appeler les méthodes d’un serveur. Il existe deux façons de désactiver la sécurité des appels implique l’utilisation de Dcomcnfg.exe pour modifier le registre, et l’autre requiert des appels à CoInitializeSecurity.
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379715"
---
# <a name="turning-off-call-security"></a><span data-ttu-id="0738c-104">Désactivation de la sécurité de l’appel</span><span class="sxs-lookup"><span data-stu-id="0738c-104">Turning Off Call Security</span></span>

<span data-ttu-id="0738c-105">La sécurité de l’appel détermine si un client a l’autorisation d’appeler les méthodes d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="0738c-105">Call security determines whether a client has permission to call a server's methods.</span></span> <span data-ttu-id="0738c-106">Il existe deux façons de désactiver la sécurité des appels : l’un implique l’utilisation de Dcomcnfg.exe pour modifier le registre, et l’autre requiert des appels à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="0738c-106">There are two ways to disable call security: One involves using Dcomcnfg.exe to modify the registry, and the other requires calls to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

-   [<span data-ttu-id="0738c-107">Désactivation de la sécurité des appels à l’aide de DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="0738c-107">Turning Off Call Security Using DCOMCNFG</span></span>](#turning-off-call-security-using-dcomcnfg)
-   [<span data-ttu-id="0738c-108">Désactivation de la sécurité des appels par programmation</span><span class="sxs-lookup"><span data-stu-id="0738c-108">Turning Off Call Security Programmatically</span></span>](#turning-off-call-security-programmatically)
-   [<span data-ttu-id="0738c-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0738c-109">Related topics</span></span>](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a><span data-ttu-id="0738c-110">Désactivation de la sécurité des appels à l’aide de DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="0738c-110">Turning Off Call Security Using DCOMCNFG</span></span>

<span data-ttu-id="0738c-111">La sécurité de l’appel peut être facilement désactivée à l’aide de Dcomcnfg.exe pour modifier le registre.</span><span class="sxs-lookup"><span data-stu-id="0738c-111">Call security can most easily be turned off by using Dcomcnfg.exe to modify the registry.</span></span> <span data-ttu-id="0738c-112">Toutefois, l’utilisation de Dcomcnfg.exe pour désactiver la sécurité fonctionne uniquement si le client et le serveur n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="0738c-112">However, using Dcomcnfg.exe to turn security off will work only if both the client and the server do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="0738c-113">En effet, lorsque la méthode **CoInitializeSecurity** est appelée, DCOM ignore les paramètres du Registre et utilise à la place les valeurs fournies à **CoInitializeSecurity** .</span><span class="sxs-lookup"><span data-stu-id="0738c-113">This is because when **CoInitializeSecurity** is called, DCOM ignores the registry settings and uses the values supplied to **CoInitializeSecurity** instead.</span></span>

<span data-ttu-id="0738c-114">Pour désactiver la sécurité avec Dcomcnfg.exe, le client et le serveur doivent tous deux définir leurs niveaux d’authentification sur aucun.</span><span class="sxs-lookup"><span data-stu-id="0738c-114">To turn off security with Dcomcnfg.exe, both the client and the server must set their Authentication Levels to None.</span></span> <span data-ttu-id="0738c-115">Les étapes suivantes doivent être effectuées :</span><span class="sxs-lookup"><span data-stu-id="0738c-115">The following steps must be completed:</span></span>

1.  <span data-ttu-id="0738c-116">Exécutez Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="0738c-116">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="0738c-117">Dans la page **applications** , sélectionnez l’application qui représente le serveur.</span><span class="sxs-lookup"><span data-stu-id="0738c-117">On the **Applications** page, select the application that represents the server.</span></span> <span data-ttu-id="0738c-118">Cliquez sur le bouton des **Propriétés** (ou double-cliquez sur l’application sélectionnée).</span><span class="sxs-lookup"><span data-stu-id="0738c-118">Click the **Properties** button (or double-click the selected application).</span></span>
3.  <span data-ttu-id="0738c-119">Cliquez sur l’onglet **General** (Général).</span><span class="sxs-lookup"><span data-stu-id="0738c-119">Click the **General** tab.</span></span>
4.  <span data-ttu-id="0738c-120">Dans la zone de liste **niveau d’authentification par défaut** , sélectionnez **(aucun)**.</span><span class="sxs-lookup"><span data-stu-id="0738c-120">From the **Default Authentication Level** list box, select **(None)**.</span></span>
5.  <span data-ttu-id="0738c-121">Cliquez sur le bouton **appliquer** pour appliquer les modifications. Toutefois, les modifications ne sont pas appliquées aux instances en cours d’exécution de l’application.</span><span class="sxs-lookup"><span data-stu-id="0738c-121">Click the **Apply** button to apply changes; however, changes are not applied to any running instances of the application.</span></span>
6.  <span data-ttu-id="0738c-122">Si le client apparaît dans la liste de la page *applications* , répétez les étapes 2 à 5, en choisissant le client au lieu du serveur pour l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="0738c-122">If the client appears on the list on the *Applications* page, repeat steps 2 through 5, choosing the client instead of the server for step 2.</span></span> <span data-ttu-id="0738c-123">Cliquez ensuite sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="0738c-123">Then click the **OK** button.</span></span> <span data-ttu-id="0738c-124">Si le client ne figure pas dans la liste, vous pouvez effectuer l’une des trois opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0738c-124">If the client is not on the list, you can do one of the following three things:</span></span>
    -   <span data-ttu-id="0738c-125">Vous pouvez définir le niveau d’authentification du client sur aucun à l’échelle de l’ordinateur à l’aide de Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="0738c-125">You can set the client's Authentication Level to None on a computer-wide basis by using Dcomcnfg.exe.</span></span> <span data-ttu-id="0738c-126">(Voir l’avertissement et la procédure ci-dessous.)</span><span class="sxs-lookup"><span data-stu-id="0738c-126">(See the warning and the procedure below.)</span></span>
    -   <span data-ttu-id="0738c-127">Vous pouvez définir le niveau d’authentification du client sur aucun par programme.</span><span class="sxs-lookup"><span data-stu-id="0738c-127">You can set the client's authentication level to None programmatically.</span></span>
    -   <span data-ttu-id="0738c-128">Vous pouvez créer une clé [AppID](appid-key.md) pour le client afin d’indiquer le niveau d’authentification None.</span><span class="sxs-lookup"><span data-stu-id="0738c-128">You can create an [AppID](appid-key.md) key for the client to indicate an authentication level of None.</span></span> <span data-ttu-id="0738c-129">(Voir [définition de la sécurité Process-Wide dans le registre](setting-processwide-security-through-the-registry.md).)</span><span class="sxs-lookup"><span data-stu-id="0738c-129">(See [Setting Process-Wide Security Through the Registry](setting-processwide-security-through-the-registry.md).)</span></span>

<span data-ttu-id="0738c-130">Pour définir le niveau d’authentification sur la valeur None à l’échelle de l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="0738c-130">To set the Authentication Level to None on a computer-wide basis:</span></span>

> [!Note]  
> <span data-ttu-id="0738c-131">La définition du niveau d’authentification à l’échelle de l’ordinateur sur aucun est extrêmement non sécurisée.</span><span class="sxs-lookup"><span data-stu-id="0738c-131">Setting the computer-wide Authentication Level to None is extremely unsecure.</span></span>

 

1.  <span data-ttu-id="0738c-132">Exécutez Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="0738c-132">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="0738c-133">Choisissez l’onglet **propriétés par défaut** .</span><span class="sxs-lookup"><span data-stu-id="0738c-133">Choose the **Default Properties** tab.</span></span>
3.  <span data-ttu-id="0738c-134">Dans la zone de liste **niveau d’authentification par défaut** , choisissez **(aucun)**.</span><span class="sxs-lookup"><span data-stu-id="0738c-134">From the **Default Authentication Level** list box, choose **(None)**.</span></span>
4.  <span data-ttu-id="0738c-135">Cliquez sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="0738c-135">Click the **OK** button.</span></span>

## <a name="turning-off-call-security-programmatically"></a><span data-ttu-id="0738c-136">Désactivation de la sécurité des appels par programmation</span><span class="sxs-lookup"><span data-stu-id="0738c-136">Turning Off Call Security Programmatically</span></span>

<span data-ttu-id="0738c-137">Pour désactiver la sécurité de l’appel par programmation, le client et le serveur doivent tous les deux appeler **CoInitializeSecurity**, en définissant le niveau d’authentification dans le paramètre *dwAuthnLevel* sur RPC \_ C \_ Authn \_ niveau \_ None.</span><span class="sxs-lookup"><span data-stu-id="0738c-137">To turn call security off programmatically, both the client and the server must call **CoInitializeSecurity**, setting the authentication level in the *dwAuthnLevel* parameter to RPC\_C\_AUTHN\_LEVEL\_NONE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0738c-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0738c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0738c-139">Désactivation de la sécurité d’activation</span><span class="sxs-lookup"><span data-stu-id="0738c-139">Turning Off Activation Security</span></span>](turning-off-activation-security.md)
</dt> </dl>

 

 




