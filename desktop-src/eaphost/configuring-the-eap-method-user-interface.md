---
title: Configuration de l’interface utilisateur de la méthode EAP
description: Explique comment configurer le demandeur en fournissant une configuration de méthode EAP à EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b82debadc075b1fcc12dad06484c0fd3617874
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106512293"
---
# <a name="configuring-the-eap-method-user-interface"></a><span data-ttu-id="0fe2e-103">Configuration de l’interface utilisateur de la méthode EAP</span><span class="sxs-lookup"><span data-stu-id="0fe2e-103">Configuring the EAP Method User Interface</span></span>

<span data-ttu-id="0fe2e-104">Cette rubrique explique comment configurer le demandeur en fournissant une configuration de méthode EAP à EAPHost.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-104">This topic explains how to configure the supplicant by supplying an EAP method configuration to EAPHost.</span></span>

<span data-ttu-id="0fe2e-105">Pour qu’un demandeur effectue une authentification basée sur EAP à l’aide d’EAPHost, un demandeur doit fournir une configuration de méthode EAP à EAPHost via la fonction [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) .</span><span class="sxs-lookup"><span data-stu-id="0fe2e-105">For a supplicant to perform an EAP-based authentication using EAPHost, a supplicant must supply an EAP method configuration to EAPHost through the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) function.</span></span>

1.  <span data-ttu-id="0fe2e-106">Pour obtenir la configuration de la méthode EAP, un demandeur interroge généralement EAPHost à l’aide de [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) pour connaître l’ensemble complet des méthodes EAP disponibles et installées sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-106">To obtain the EAP method configuration, a supplicant typically queries EAPHost using [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) to learn the complete set of EAP methods that are available and installed on the local machine.</span></span> <span data-ttu-id="0fe2e-107">La liste des méthodes est généralement présentée à l’utilisateur dans une zone combinée ou un autre contrôle d’interface utilisateur qui permet à l’utilisateur de sélectionner la méthode de votre choix.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-107">The list of methods is typically presented to the user in a combination box or other UI control that allows the user to select the method they want.</span></span>
    > [!Note]  
    > <span data-ttu-id="0fe2e-108">Le demandeur peut choisir de filtrer la liste affichée des méthodes en fonction des bits de propriété de méthode indiqués dans informations sur la **\_ méthode EAP \_ . eapProperties**.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-108">The supplicant may choose to filter the displayed list of methods based on the method property bits indicated in **EAP\_METHOD\_INFO.eapProperties**.</span></span> <span data-ttu-id="0fe2e-109">Certaines méthodes peuvent ne pas convenir aux caractéristiques de sécurité du transport fournies par le demandeur, par exemple.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-109">Some methods may not be appropriate for the security characteristics of the transport provided by the supplicant, for example.</span></span>

     

2.  <span data-ttu-id="0fe2e-110">Une fois que le contrôle d’interface utilisateur est rempli avec l’ensemble de méthodes EAP possibles, l’utilisateur sélectionne la méthode qu’il souhaite configurer.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-110">Once the UI control is populated with the set of possible EAP methods, the user selects the method they want to configure.</span></span> <span data-ttu-id="0fe2e-111">En règle générale, le demandeur fournit un bouton de **configuration** ou de **Propriétés** permettant à l’utilisateur d’accéder aux propriétés de configuration de la méthode EAP sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-111">Typically, the supplicant provides a **Configuration** or **Properties** button for the user to access configuration properties of the selected EAP method.</span></span>
    > [!Note]
    > <span data-ttu-id="0fe2e-112">Le demandeur est conscient qu’il existe des propriétés configurables par l’utilisateur basées sur l’activation du bit **eapPropSupportsConfig** dans informations sur la **\_ méthode EAP \_ . eapProperties**.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-112">The supplicant is aware that there are user-configurable properties based on the **eapPropSupportsConfig** bit being enabled in **EAP\_METHOD\_INFO.eapProperties**.</span></span>
    >
    > <span data-ttu-id="0fe2e-113">Pour plus d’informations, consultez Propriétés de la [**méthode EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="0fe2e-113">For more information, see [**EAP Method Properties**](eap-method-properties.md).</span></span>

     

3.  <span data-ttu-id="0fe2e-114">Lorsque l’utilisateur clique sur le contrôle d’interface utilisateur approprié, le demandeur appelle [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), en passant à la fonction la valeur **HWND** pour la propre interface utilisateur du demandeur, la structure de [**\_ \_ type de méthode EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) obtenue à partir de la structure de la requête vers la structure d' [**\_ \_ informations de méthode EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) et d’autres paramètres requis.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-114">When the user clicks the appropriate UI control, the supplicant calls [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), passing into the function the **HWND** value for the supplicant's own UI, the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure obtained from the query to [**EAP\_METHOD\_INFO**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) structure and other required parameters.</span></span>
4.  <span data-ttu-id="0fe2e-115">L’appel de [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) appelle l’interface utilisateur de configuration de la méthode EAP.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-115">Calling [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) invokes an EAP method's own configuration UI.</span></span> <span data-ttu-id="0fe2e-116">Au retour de **EapHostPeerInvokeConfigUI**, la fonction retourne un objet blob de configuration de méthode EAP en tant que paramètre out.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-116">On return from **EapHostPeerInvokeConfigUI**, the function will return an EAP method configuration BLOB as an out-parameter.</span></span>
5.  <span data-ttu-id="0fe2e-117">Le demandeur stocke l’objet BLOB de configuration, ainsi que la structure de [**\_ \_ type de méthode EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) à utiliser avec [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="0fe2e-117">The supplicant stores the configuration BLOB, along with the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure for use with [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>
6.  <span data-ttu-id="0fe2e-118">La méthode précise pour le stockage de l’objet BLOB configuration dépend entièrement du demandeur.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-118">The precise method for storing the configuraiton BLOB is entirely up to the supplicant.</span></span> <span data-ttu-id="0fe2e-119">Toutefois, le demandeur doit toujours stocker la configuration de manière sécurisée et appropriée pour les données de configuration d’authentification du système et des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0fe2e-119">However, the supplicant should always store the configuration in a suitable, secure manner appropriate for system and user authentication configuration data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fe2e-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0fe2e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fe2e-121">Activation de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="0fe2e-121">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="0fe2e-122">Implémentation de la prise en charge de In-Band NAP pour les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="0fe2e-122">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="0fe2e-123">Implémentation de la prise en charge NAP pour les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="0fe2e-123">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="0fe2e-124">Transfert de données entre le demandeur et les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="0fe2e-124">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="0fe2e-125">Demandeurs EAPHost</span><span class="sxs-lookup"><span data-stu-id="0fe2e-125">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




