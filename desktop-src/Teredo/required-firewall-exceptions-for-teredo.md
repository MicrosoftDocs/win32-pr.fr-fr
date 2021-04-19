---
title: Exceptions de pare-feu requises pour Teredo
description: Pour qu’une application reçoive le trafic Teredo, l’application doit être autorisée à recevoir le trafic IPv6 dans le pare-feu de l’hôte, et l’application est requise pour définir le niveau de protection de l’option de socket \_ \_ sur « niveau de protection non \_ \_ restreint ».
ms.assetid: 2fc74d86-9696-4ba9-adbe-e5558ae7d7c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbc2fcf0f7c8b1f5fe51afc056dc8c8ff7c7916a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509668"
---
# <a name="required-firewall-exceptions-for-teredo"></a><span data-ttu-id="87742-103">Exceptions de pare-feu requises pour Teredo</span><span class="sxs-lookup"><span data-stu-id="87742-103">Required Firewall Exceptions for Teredo</span></span>

<span data-ttu-id="87742-104">Pour qu’une application reçoive le trafic Teredo, l’application doit être autorisée à recevoir le trafic IPv6 dans le pare-feu de l’hôte, et l’application est requise pour définir le [ \_ \_ niveau de protection](/windows/desktop/WinSock/ipv6-protection-level) de l’option de socket sur « niveau de protection non \_ \_ restreint ».</span><span class="sxs-lookup"><span data-stu-id="87742-104">For an application to receive Teredo traffic, the application must be permitted to receive IPv6 traffic in the host firewall, and the application is required to set the socket option [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) to 'PROTECTION\_LEVEL\_UNRESTRICTED'.</span></span> <span data-ttu-id="87742-105">Pour activer ce type de scénario, les exceptions de pare-feu détaillées dans ce document doivent être implémentées.</span><span class="sxs-lookup"><span data-stu-id="87742-105">To enable this type of scenario, the firewall exceptions detailed in this document must be implemented.</span></span>

<span data-ttu-id="87742-106">Les configurations de pare-feu suivantes sont requises pour assurer une interopérabilité fluide entre un pare-feu et Teredo :</span><span class="sxs-lookup"><span data-stu-id="87742-106">The following firewall configurations are required to ensure smooth interoperation between a firewall and Teredo:</span></span>

-   <span data-ttu-id="87742-107">Le pare-feu client doit permettre la résolution de teredo.ipv6.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="87742-107">The client firewall must allow resolution of teredo.ipv6.microsoft.com.</span></span>
-   <span data-ttu-id="87742-108">Le port UDP 3544 doit être ouvert pour s’assurer que les clients Teredo peuvent communiquer correctement avec le serveur Teredo.</span><span class="sxs-lookup"><span data-stu-id="87742-108">UDP Port 3544 must be open to ensure that Teredo clients can successfully communicate with the Teredo server.</span></span>
-   <span data-ttu-id="87742-109">Le pare-feu doit récupérer les ports UDP dynamiques utilisés par le service Teredo sur l’ordinateur local en appelant la fonction [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) . les ports appropriés sont de type FWPM du \_ \_ port système \_ TEREDO.</span><span class="sxs-lookup"><span data-stu-id="87742-109">The firewall must retrieve dynamic UDP ports used by Teredo service on the local machine by calling the [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) function; relevant ports are of type FWPM\_SYSTEM\_PORT\_TEREDO.</span></span> <span data-ttu-id="87742-110">La fonction **FwpmSystemPortsGet0** doit être implémentée à la place des fonctions [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) ou [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) désormais dépréciées.</span><span class="sxs-lookup"><span data-stu-id="87742-110">The **FwpmSystemPortsGet0** function should be implemented in place of the now deprecated [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) or [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) functions.</span></span>
-   <span data-ttu-id="87742-111">Le pare-feu permet au système d’envoyer et de recevoir des paquets UDP/IPv4 au port UDP 1900 sur le sous-réseau local, car cela permet au trafic de découverte UPnP de circuler et d’améliorer les vitesses de connectivité.</span><span class="sxs-lookup"><span data-stu-id="87742-111">The firewall permits the system to send and receive UDP/IPv4 packets to UDP port 1900 on the local subnet as this allows UPnP discovery traffic to flow and has the potential to improve connectivity rates.</span></span>
    > [!Note]  
    > <span data-ttu-id="87742-112">Si cette condition n’est pas remplie, les scénarios susceptibles de rencontrer des problèmes de compatibilité impliquant la communication entre certains types NAT sont introduits. en particulier entre les NAT symétriques et les NAT restreints.</span><span class="sxs-lookup"><span data-stu-id="87742-112">If this condition is not met, the potential for scenarios to encounter compatibility issues involving communication between certain NAT types is introduced; specifically between Symmetric NATs and Restricted NATs.</span></span> <span data-ttu-id="87742-113">Alors que les NAT symétriques sont populaires dans les zones réactives et que les traducteurs d’adresses réseau sont populaires dans les maisons, la communication entre les deux risque d’échouer sur le côté du NAT restreint.</span><span class="sxs-lookup"><span data-stu-id="87742-113">While Symmetric NATs are popular in hotspots and Restricted NATs are popular in homes, communication between the two has the potential to fault on the side of the Restricted NAT.</span></span>

     

-   <span data-ttu-id="87742-114">Les exceptions entrantes et sortantes ICMPv6 « demande ECHO » et « réponse à écho » doivent être activées.</span><span class="sxs-lookup"><span data-stu-id="87742-114">Incoming and outgoing ICMPv6 "Echo Request" and "Echo Reply" exceptions must be enabled.</span></span> <span data-ttu-id="87742-115">Ces exceptions sont nécessaires pour s’assurer qu’un client Teredo peut agir en tant que relais Teredo spécifique à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="87742-115">These exceptions are necessary to ensure that a Teredo client can act as a Teredo host-specific relay.</span></span> <span data-ttu-id="87742-116">Un relais Teredo spécifique à l’hôte peut être identifié par l’adresse IPv6 native supplémentaire ou une adresse 6to4 fournie avec l’adresse Teredo.</span><span class="sxs-lookup"><span data-stu-id="87742-116">A Teredo host-specific relay can be identified by the additional native IPv6 address or a 6to4 address supplied with the Teredo address.</span></span>

<span data-ttu-id="87742-117">Les pare-feu clients doivent prendre en charge les messages d’erreur ICMPv6 et les fonctions de découverte suivants selon la norme RFC 4443 :</span><span class="sxs-lookup"><span data-stu-id="87742-117">Client firewalls must support the following ICMPv6 error messages and discovery functions per RFC 4443:</span></span>



| <span data-ttu-id="87742-118">Code</span><span class="sxs-lookup"><span data-stu-id="87742-118">Code</span></span>    | <span data-ttu-id="87742-119">Description</span><span class="sxs-lookup"><span data-stu-id="87742-119">Description</span></span>                                    |
|---------|------------------------------------------------|
| <span data-ttu-id="87742-120">135/136</span><span class="sxs-lookup"><span data-stu-id="87742-120">135/136</span></span> | <span data-ttu-id="87742-121">Sollicitation et publication du voisin ICMPV6</span><span class="sxs-lookup"><span data-stu-id="87742-121">ICMPV6 Neighbor Solicitation and Advertisement</span></span> |
| <span data-ttu-id="87742-122">133/134</span><span class="sxs-lookup"><span data-stu-id="87742-122">133/134</span></span> | <span data-ttu-id="87742-123">Sollicitation de routeur et publication</span><span class="sxs-lookup"><span data-stu-id="87742-123">Router Solicitation and Advertisement</span></span>          |
| <span data-ttu-id="87742-124">128/129</span><span class="sxs-lookup"><span data-stu-id="87742-124">128/129</span></span> | <span data-ttu-id="87742-125">Demande et réponse d’écho ICMPV6</span><span class="sxs-lookup"><span data-stu-id="87742-125">ICMPV6 Echo Request and Reply</span></span>                  |
| <span data-ttu-id="87742-126">1</span><span class="sxs-lookup"><span data-stu-id="87742-126">1</span></span>       | <span data-ttu-id="87742-127">Destination inaccessible</span><span class="sxs-lookup"><span data-stu-id="87742-127">Destination Unreachable</span></span>                        |
| <span data-ttu-id="87742-128">2</span><span class="sxs-lookup"><span data-stu-id="87742-128">2</span></span>       | <span data-ttu-id="87742-129">Paquet trop volumineux</span><span class="sxs-lookup"><span data-stu-id="87742-129">Packet Too Large</span></span>                               |
| <span data-ttu-id="87742-130">3</span><span class="sxs-lookup"><span data-stu-id="87742-130">3</span></span>       | <span data-ttu-id="87742-131">Temps dépassé</span><span class="sxs-lookup"><span data-stu-id="87742-131">Time Exceeded</span></span>                                  |
| <span data-ttu-id="87742-132">4</span><span class="sxs-lookup"><span data-stu-id="87742-132">4</span></span>       | <span data-ttu-id="87742-133">Paramètre non valide</span><span class="sxs-lookup"><span data-stu-id="87742-133">Invalid Parameter</span></span>                              |



 

<span data-ttu-id="87742-134">Si ces messages ne peuvent pas être explicitement autorisés, l’exemption de tous les messages ICMPv6 doit être activée sur le pare-feu.</span><span class="sxs-lookup"><span data-stu-id="87742-134">If these messages cannot be specifically allowed, then the exemption of all ICMPv6 messages should be enabled on the firewall.</span></span> <span data-ttu-id="87742-135">En outre, le pare-feu de l’hôte peut remarquer que les paquets classés par codes 135/136 ou 133/134 proviennent du service en mode utilisateur **iphlpsvc** et non de la pile.</span><span class="sxs-lookup"><span data-stu-id="87742-135">Additionally, the host firewall may notice that the packets classified by codes 135/136 or 133/134 originate from, or are targeted to, the user mode service **iphlpsvc** and not from the stack.</span></span> <span data-ttu-id="87742-136">Ces paquets ne doivent pas être supprimés par le pare-feu hôte.</span><span class="sxs-lookup"><span data-stu-id="87742-136">These packets must not be dropped by the host firewall.</span></span> <span data-ttu-id="87742-137">Le service Teredo est implémenté principalement dans le service d’assistance IP « mode utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="87742-137">The Teredo service is implemented primarily within the 'user mode' IP Helper service.</span></span>

<span data-ttu-id="87742-138">À l’aide de l’API du pare-feu Windows [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) pour énumérer toutes les règles avec l’indicateur de parcours Edge défini, toutes les applications qui souhaitent écouter le trafic non sollicité sont énumérées pour l’exception de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="87742-138">Using the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) Windows Firewall API to enumerate all rules with the Edge Traversal flag set, all applications that want to listen for unsolicited traffic are enumerated for the firewall exception.</span></span> <span data-ttu-id="87742-139">Des informations spécifiques concernant l’utilisation de l’option de traversée latérale sont détaillées dans [réception de trafic non sollicité sur Teredo](receiving-unsolicited-traffic-over-teredo.md).</span><span class="sxs-lookup"><span data-stu-id="87742-139">Specific information regarding the use of the Edge Traversal option is detailed in [Receiving Unsolicited Traffic Over Teredo](receiving-unsolicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="87742-140">Les rappels ne sont pas associés au code d’énumération d’exemple suivant ; Il est fortement recommandé que les pare-feu tiers effectuent l’énumération régulièrement, ou chaque fois que le pare-feu détecte une nouvelle application tentant de traverser le pare-feu.</span><span class="sxs-lookup"><span data-stu-id="87742-140">Callbacks are not associated with the following sample enumeration code; it is strongly recommended that third party firewalls perform the enumeration periodically, or whenever the firewall detects a new application attempting to go through the firewall.</span></span>


```C++
#include <windows.h>
#include <objbase.h>
#include <stdio.h>
#include <atlcomcli.h>
#include <strsafe.h>
#include <netfw.h>

#define NET_FW_IP_PROTOCOL_TCP_NAME L"TCP"
#define NET_FW_IP_PROTOCOL_UDP_NAME L"UDP"

#define NET_FW_RULE_DIR_IN_NAME L"In"
#define NET_FW_RULE_DIR_OUT_NAME L"Out"

#define NET_FW_RULE_ACTION_BLOCK_NAME L"Block"
#define NET_FW_RULE_ACTION_ALLOW_NAME L"Allow"

#define NET_FW_RULE_ENABLE_IN_NAME L"TRUE"
#define NET_FW_RULE_DISABLE_IN_NAME L"FALSE"

#import "netfw.tlb"

void DumpFWRulesInCollection(long Allprofiletypes, NetFwPublicTypeLib::INetFwRulePtr FwRule)
{
    variant_t InterfaceArray;
    variant_t InterfaceString;    

    if(FwRule->Profiles == Allprofiletypes)
    {
        wprintf(L"---------------------------------------------\n");
        wprintf(L"Name:             %s\n", (BSTR)FwRule->Name);        
        wprintf(L"Description:      %s\n", (BSTR)FwRule->Description);
        wprintf(L"Application Name: %s\n", (BSTR)FwRule->ApplicationName);
        wprintf(L"Service Name:     %s\n", (BSTR)FwRule->serviceName);

        switch(FwRule->Protocol)
        {
        case NET_FW_IP_PROTOCOL_TCP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_TCP_NAME);
            break;
        case NET_FW_IP_PROTOCOL_UDP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_UDP_NAME);
            break;
        default:
            break;
        }

        if(FwRule->Protocol != NET_FW_IP_VERSION_V4 && FwRule->Protocol != NET_FW_IP_VERSION_V6)
        {
            wprintf(L"Local Ports:      %s\n", (BSTR)FwRule->LocalPorts);
            wprintf(L"Remote Ports:     %s\n", (BSTR)FwRule->RemotePorts);
        }
        
        wprintf(L"LocalAddresses:   %s\n", (BSTR)FwRule->LocalAddresses);
        wprintf(L"RemoteAddresses:  %s\n", (BSTR)FwRule->RemoteAddresses);
        wprintf(L"Profile:          %d\n", Allprofiletypes);
        

        if(FwRule->Protocol == NET_FW_IP_VERSION_V4 || FwRule->Protocol == NET_FW_IP_VERSION_V6)
        {
            wprintf(L"ICMP TypeCode:    %s\n", (BSTR)FwRule->IcmpTypesAndCodes);
        }

        switch(FwRule->Direction)
        {
        case NET_FW_RULE_DIR_IN:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_IN_NAME);
            break;
        case NET_FW_RULE_DIR_OUT:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_OUT_NAME);
            break;
        default:
            break;
        }

        switch(FwRule->Action)
        {
        case NET_FW_ACTION_BLOCK:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_BLOCK_NAME);
            break;
        case NET_FW_ACTION_ALLOW:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_ALLOW_NAME);
            break;
        default:
            break;
        }
        
        InterfaceArray = FwRule->Interfaces;

        if(InterfaceArray.vt != VT_EMPTY)
        {
            SAFEARRAY    *pSa = NULL;
            long index = 0;

            pSa = InterfaceArray.parray;

            for(long index= pSa->rgsabound->lLbound; index < (long)pSa->rgsabound->cElements; index++)
            {
                SafeArrayGetElement(pSa, &index, &InterfaceString);
                wprintf(L"Interfaces:       %s\n", (BSTR)InterfaceString.bstrVal);
            }
        }
        wprintf(L"Interface Types:  %s\n", (BSTR)FwRule->InterfaceTypes);
        if(FwRule->Enabled)
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_ENABLE_IN_NAME);
        }
        else
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_DISABLE_IN_NAME);
        }
        wprintf(L"Grouping:         %s\n", (BSTR)FwRule->Grouping);
        wprintf(L"Edge:             %s\n", (BSTR)FwRule->EdgeTraversal);
    }
}

int __cdecl main()
{
    HRESULT hr;
    BOOL fComInitialized = FALSE;
    ULONG cFetched = 0; 
    CComVariant var;
    long Allprofiletypes = 0;

    try
    {
        IUnknownPtr pEnumerator = NULL;
        IEnumVARIANT* pVariant = NULL;
        NetFwPublicTypeLib::INetFwPolicy2Ptr sipFwPolicy2;

        //
        // Initialize the COM library on the current thread.
        //
        hr = CoInitialize(NULL);
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        fComInitialized = TRUE;
        
        hr = sipFwPolicy2.CreateInstance("HNetCfg.FwPolicy2");
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        Allprofiletypes = NET_FW_PROFILE2_ALL; // 0x7FFFFFFF
        
        printf("The number of rules in the Windows Firewall are %d\n", sipFwPolicy2->Rules->Count);

        pEnumerator = sipFwPolicy2->Rules->Get_NewEnum();

        if(pEnumerator)
        {
            hr = pEnumerator->QueryInterface(__uuidof(IEnumVARIANT), (void **) &pVariant);
        }

        while(SUCCEEDED(hr) && hr != S_FALSE)
        {        
            NetFwPublicTypeLib::INetFwRulePtr sipFwRule;

            var.Clear();
            hr = pVariant->Next(1, &var, &cFetched);
            if (S_FALSE != hr)
            {
                if (SUCCEEDED(hr))
                {
                    hr = var.ChangeType(VT_DISPATCH);
                }
                if (SUCCEEDED(hr))
                {
                    hr = (V_DISPATCH(&var))->QueryInterface(__uuidof(INetFwRule), reinterpret_cast<void**>(&sipFwRule));
                }

                if (SUCCEEDED(hr))
                {
                    DumpFWRulesInCollection(Allprofiletypes, sipFwRule);
                }
            }
        }
    }
    catch(_com_error& e)
    {
        printf ("Error. HRESULT message is: %s (0x%08lx)\n", e.ErrorMessage(), e.Error());
        if (e.ErrorInfo())
        {
            printf ("Description: %s\n", (char *)e.Description());
        }
    }
    if (fComInitialized)
    {
        CoUninitialize();
    }
    return 0;
}

```



 

 