---
title: Exceptions de pare-feu requises pour Teredo
description: Pour qu’une application reçoive le trafic Teredo, l’application doit être autorisée à recevoir le trafic IPv6 dans le pare-feu de l’hôte, et l’application est requise pour définir le niveau de protection de l’option de socket \_ \_ sur « niveau de protection non \_ \_ restreint ».
ms.assetid: 2fc74d86-9696-4ba9-adbe-e5558ae7d7c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbc2fcf0f7c8b1f5fe51afc056dc8c8ff7c7916a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193452"
---
# <a name="required-firewall-exceptions-for-teredo"></a>Exceptions de pare-feu requises pour Teredo

Pour qu’une application reçoive le trafic Teredo, l’application doit être autorisée à recevoir le trafic IPv6 dans le pare-feu de l’hôte, et l’application est requise pour définir le [ \_ \_ niveau de protection](/windows/desktop/WinSock/ipv6-protection-level) de l’option de socket sur « niveau de protection non \_ \_ restreint ». Pour activer ce type de scénario, les exceptions de pare-feu détaillées dans ce document doivent être implémentées.

Les configurations de pare-feu suivantes sont requises pour assurer une interopérabilité fluide entre un pare-feu et Teredo :

-   Le pare-feu client doit permettre la résolution de teredo.ipv6.microsoft.com.
-   Le port UDP 3544 doit être ouvert pour s’assurer que les clients Teredo peuvent communiquer correctement avec le serveur Teredo.
-   Le pare-feu doit récupérer les ports UDP dynamiques utilisés par le service Teredo sur l’ordinateur local en appelant la fonction [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) . les ports appropriés sont de type FWPM du \_ \_ port système \_ TEREDO. La fonction **FwpmSystemPortsGet0** doit être implémentée à la place des fonctions [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) ou [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) désormais dépréciées.
-   Le pare-feu permet au système d’envoyer et de recevoir des paquets UDP/IPv4 au port UDP 1900 sur le sous-réseau local, car cela permet au trafic de découverte UPnP de circuler et d’améliorer les vitesses de connectivité.
    > [!Note]  
    > Si cette condition n’est pas remplie, les scénarios susceptibles de rencontrer des problèmes de compatibilité impliquant la communication entre certains types NAT sont introduits. en particulier entre les NAT symétriques et les NAT restreints. Alors que les NAT symétriques sont populaires dans les zones réactives et que les traducteurs d’adresses réseau sont populaires dans les maisons, la communication entre les deux risque d’échouer sur le côté du NAT restreint.

     

-   Les exceptions entrantes et sortantes ICMPv6 « demande ECHO » et « réponse à écho » doivent être activées. Ces exceptions sont nécessaires pour s’assurer qu’un client Teredo peut agir en tant que relais Teredo spécifique à l’hôte. Un relais Teredo spécifique à l’hôte peut être identifié par l’adresse IPv6 native supplémentaire ou une adresse 6to4 fournie avec l’adresse Teredo.

Les pare-feu clients doivent prendre en charge les messages d’erreur ICMPv6 et les fonctions de découverte suivants selon la norme RFC 4443 :



| Code    | Description                                    |
|---------|------------------------------------------------|
| 135/136 | Sollicitation et publication du voisin ICMPV6 |
| 133/134 | Sollicitation de routeur et publication          |
| 128/129 | Demande et réponse d’écho ICMPV6                  |
| 1       | Destination inaccessible                        |
| 2       | Paquet trop volumineux                               |
| 3       | Temps dépassé                                  |
| 4       | Paramètre non valide                              |



 

Si ces messages ne peuvent pas être explicitement autorisés, l’exemption de tous les messages ICMPv6 doit être activée sur le pare-feu. En outre, le pare-feu de l’hôte peut remarquer que les paquets classés par codes 135/136 ou 133/134 proviennent du service en mode utilisateur **iphlpsvc** et non de la pile. Ces paquets ne doivent pas être supprimés par le pare-feu hôte. Le service Teredo est implémenté principalement dans le service d’assistance IP « mode utilisateur ».

à l’aide de l’API de pare-feu [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) Windows pour énumérer toutes les règles avec l’indicateur de parcours Edge défini, toutes les applications qui souhaitent écouter le trafic non sollicité sont énumérées pour l’exception de pare-feu. Des informations spécifiques concernant l’utilisation de l’option de traversée latérale sont détaillées dans [réception de trafic non sollicité sur Teredo](receiving-unsolicited-traffic-over-teredo.md).

Les rappels ne sont pas associés au code d’énumération d’exemple suivant ; Il est fortement recommandé que les pare-feu tiers effectuent l’énumération régulièrement, ou chaque fois que le pare-feu détecte une nouvelle application tentant de traverser le pare-feu.


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



 

 