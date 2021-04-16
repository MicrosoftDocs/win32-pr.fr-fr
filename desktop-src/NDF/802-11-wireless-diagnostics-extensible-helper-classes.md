---
title: Classes d’assistance extensibles pour les diagnostics sans fil 802,11
description: L’infrastructure de diagnostics sans fil intégrée a deux points d’extension. Problèmes ClassDiagnoses de l’application auxiliaire ClassPurposeRevised Native WiFi (RNWF) associés aux extensions de connectivité 802,11.
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde49561c68044157c9d518571b8241c49dcf25
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104507811"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a>Classes d’assistance extensibles pour les diagnostics sans fil 802,11

L’infrastructure de diagnostics sans fil intégrée a deux points d’extension.

| Classe d’assistance parente                                | Objectif                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| Classe d’assistance extensible Native WiFi (RNWF) révisée | Diagnostique les problèmes liés aux extensions de connectivité 802,11.       |
| Classe d’assistance extensible L2Security                 | Diagnostique les problèmes liés aux extensions de protocole de sécurité de couche 2. |



 

> [!Note]  
> Une classe d’assistance tierce doit s’inscrire auprès des deux classes d’assistance parentes pour s’assurer que la classe tierce est appelée. Pour plus d’informations sur l’inscription, consultez [Registering NDF Helper Class extensions](registering-ndf-helper-class-extensions.md).

 

## <a name="rnwf-extensible-helper-class"></a>Classe d’assistance extensible RNWF

Nom de la classe d’assistance parente

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

La classe d’assistance extensible Native WiFi (RNWF) révisée est le parent des classes d’assistance tierces qui diagnostiquent les problèmes liés à l’extension des protocoles 802,11 utilisés par le WiFi natif.

Les deux attributs clés fournis par la classe d’assistance RNWF sont le GUID de l’interface dans laquelle le problème s’est produit et le contexte de connexion.

-   GUID de l’interface : cet attribut est nommé « ID d’interface » et est de type **au \_ GUID**.

-   Contexte de connexion : cet attribut est nommé ID réseau et est de type \_ chaîne d’octets \_ . Cette chaîne est en fait une mémoire tampon de la structure de l' \_ \_ ID WLAN WDIAG IHV \_ définie dans Wlanihv. h. Cette structure est définie comme suit.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ L' \_ indicateur d’ID WLAN IHV \_ \_ \_ \_ activé** pour la sécurité est la seule valeur **dwFlags** possible.

 

L’attribut correspondant pour la classe d’assistance tierce doit être identique à l’ID de service de son module logiciel correspondant. Il s’agit également du même nom que le tiers doit être inscrit dans le registre. Les diagnostics sans fil interrogent l’ID de service pendant la session sans fil dans laquelle le problème s’est produit. Les informations sont retournées à NDF, qui détermine si la classe d’assistance tierce est présente et inscrite, puis l’appelle.

Le tableau suivant répertorie les attributs correspondants pour la classe d’assistance extensible RNWF.



| Nom          | Type    | Valeur                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | SZ de REG \_ | \[\_Chaîne GUID \_ DiagnosticsID |



 

## <a name="l2security-extensible-helper-class"></a>Classe d’assistance extensible L2Security

Nom de la classe d’assistance parente

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

La classe d’assistance extensible Layer 2 Security (L2Security) est le parent des classes d’assistance tierces qui diagnostiquent les problèmes liés aux services et modules logiciels correspondants qui remplacent les fonctionnalités de sécurité de couche 2.

Les deux attributs clés fournis par la classe d’assistance de sécurité de couche 2 sont le GUID de l’interface dans laquelle le problème s’est produit et le contexte de connexion.

-   GUID de l’interface : cet attribut est nommé « ID d’interface » et est de type **au \_ GUID**.

-   Contexte de connexion : cet attribut est nommé ID réseau et est de type \_ chaîne d’octets \_ . Cette chaîne est en fait une mémoire tampon de la structure de l' \_ \_ ID WLAN WDIAG IHV \_ définie dans wlanihv. h. Cette structure est définie comme suit.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ L' \_ indicateur d’ID WLAN IHV \_ \_ \_ \_ activé** pour la sécurité est la seule valeur **dwFlags** possible.

 

L’attribut correspondant pour la classe d’assistance tierce doit être identique à l’ID de service de son module logiciel correspondant. Il s’agit également du même nom que le tiers doit être inscrit dans le registre. Les diagnostics sans fil interrogent l’ID de service pendant la session sans fil dans laquelle le problème s’est produit. Les informations sont retournées à NDF, qui détermine si la classe d’assistance tierce est présente et inscrite, puis l’appelle.

Le tableau suivant répertorie les attributs correspondants pour la classe d’assistance extensible de sécurité de couche 2.



| Nom          | Type    | Valeur                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | SZ de REG \_ | \[\_Chaîne GUID \_ DiagnosticsID |



 

## <a name="matching-attributes"></a>Attributs correspondants

**DiagnosticsID**

802,11 les diagnostics sans fil interrogent le *DiagnosticsID* à partir du service Wi-Fi natif principal afin de déterminer si des extensions ou des modules de sécurité tiers sont installés et impliqués dans la connexion. Les diagnostics sans fil fournissent alors des informations sur ces classes d’assistance tierces à l’aide du *DiagnosticsID* en tant qu’attribut correspondant. Toutes les classes d’assistance tierces doivent être incluses dans et installées avec le package de pilotes associé. Le *DiagnosticsID* sera défini dans le fichier INF de miniport comme clé de Registre dans la directive [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) .

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

Cette clé définit l’ID de la classe d’assistance sans fil pour le module de logiciel tiers. Cette clé est facultative pour l’infrastructure d’extensibilité, mais elle est nécessaire si l’implémentation comprend une classe d’assistance sans fil IHV qui se connecte à NDF et peut diagnostiquer les problèmes de connectivité liés aux extensions sans fil ou de sécurité RNWF. Les classes d’assistance de diagnostic WLAN MS interrogent cet ID à partir du service de configuration automatique sans fil lorsque les modules IHV sont installés et fournissent cet ID en tant que référence ou attribut correspondant à NDF au cours d’une session de diagnostic pour que NDF puisse appeler la classe d’assistance sans fil tierce appropriée lorsque cela est nécessaire.

**\[\_Chaîne GUID \_ DiagnosticsID\]**

Cette valeur doit être une chaîne de toutes les lettres majuscules. Par exemple, « {12345678-9ABC-DEF0-1234-56789ABCDEF0} ».

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a>Étendue des classes d’assistance de diagnostic sans fil 802,11

les classes d’assistance de diagnostic sans fil 802,11 diagnostiquent actuellement les problèmes de réseau sans fil dans les domaines suivants.

-   Les problèmes de connectivité 802,11, y compris l’Association 802,11, l’authentification 802,11, les paramètres de sécurité 802,11 relatifs aux normes 802,11 & protocoles pris en charge en mode natif dans le système d’exploitation et les problèmes de performances.
-   Problèmes de sécurité de couche 2 concernant les configurations 802.1 x et problèmes liés à l’authentification de couche 2 à l’aide de méthodes prises en charge en mode natif sur Windows Vista et Windows Server 2008.
-   Incompatibilité de configuration dans les paramètres de profil entre le client et le point d’accès ou l’infrastructure réseau et les services.

les classes d’assistance de diagnostic sans fil 802,11 ne diagnostiquent pas actuellement les problèmes de réseau sans fil dans les domaines suivants.

-   Problèmes liés aux extensions 802,11 tierces, y compris les paramètres de profil ou de pilote associés à ces extensions.
-   Problèmes liés aux méthodes EAP tierces.
-   Problèmes liés au pilote miniport sans fil.
-   Tout protocole de sécurité 802,11 et de couche 2 ou des problèmes liés aux normes qui ne sont pas pris en charge en mode natif.
-   Problèmes au niveau du système ou du composant qui peuvent avoir un impact sur la connectivité sans fil, tels que la gestion de l’alimentation, l’espace disque insuffisant, les conditions de mémoire et les problèmes matériels.

En outre, 802,11 Diagnostics sans fil n’analyse pas les cas [**utilisation élevée du**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) . Les problèmes de performances sans fil identifiés seront analysés et signalés en tant que cas [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) .

 

 




