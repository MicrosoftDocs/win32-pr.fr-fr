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
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a><span data-ttu-id="3bf12-103">Classes d’assistance extensibles pour les diagnostics sans fil 802,11</span><span class="sxs-lookup"><span data-stu-id="3bf12-103">802.11 Wireless Diagnostics Extensible Helper Classes</span></span>

<span data-ttu-id="3bf12-104">L’infrastructure de diagnostics sans fil intégrée a deux points d’extension.</span><span class="sxs-lookup"><span data-stu-id="3bf12-104">The built-in wireless diagnostics infrastructure has two extension points.</span></span>

| <span data-ttu-id="3bf12-105">Classe d’assistance parente</span><span class="sxs-lookup"><span data-stu-id="3bf12-105">Parent Helper Class</span></span>                                | <span data-ttu-id="3bf12-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="3bf12-106">Purpose</span></span>                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="3bf12-107">Classe d’assistance extensible Native WiFi (RNWF) révisée</span><span class="sxs-lookup"><span data-stu-id="3bf12-107">Revised Native Wifi (RNWF) Extensible Helper Class</span></span> | <span data-ttu-id="3bf12-108">Diagnostique les problèmes liés aux extensions de connectivité 802,11.</span><span class="sxs-lookup"><span data-stu-id="3bf12-108">Diagnoses issues related to 802.11 connectivity extensions.</span></span>       |
| <span data-ttu-id="3bf12-109">Classe d’assistance extensible L2Security</span><span class="sxs-lookup"><span data-stu-id="3bf12-109">L2Security Extensible Helper Class</span></span>                 | <span data-ttu-id="3bf12-110">Diagnostique les problèmes liés aux extensions de protocole de sécurité de couche 2.</span><span class="sxs-lookup"><span data-stu-id="3bf12-110">Diagnoses issues related to Layer 2 security protocol extensions.</span></span> |



 

> [!Note]  
> <span data-ttu-id="3bf12-111">Une classe d’assistance tierce doit s’inscrire auprès des deux classes d’assistance parentes pour s’assurer que la classe tierce est appelée.</span><span class="sxs-lookup"><span data-stu-id="3bf12-111">A third-party helper class should register with both parent helper classes to ensure that the third-party class gets called.</span></span> <span data-ttu-id="3bf12-112">Pour plus d’informations sur l’inscription, consultez [Registering NDF Helper Class extensions](registering-ndf-helper-class-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="3bf12-112">For more information about registration, see [Registering NDF Helper Class Extensions](registering-ndf-helper-class-extensions.md).</span></span>

 

## <a name="rnwf-extensible-helper-class"></a><span data-ttu-id="3bf12-113">Classe d’assistance extensible RNWF</span><span class="sxs-lookup"><span data-stu-id="3bf12-113">RNWF Extensible Helper Class</span></span>

<span data-ttu-id="3bf12-114">Nom de la classe d’assistance parente</span><span class="sxs-lookup"><span data-stu-id="3bf12-114">Parent Helper Class Name</span></span>

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

<span data-ttu-id="3bf12-115">La classe d’assistance extensible Native WiFi (RNWF) révisée est le parent des classes d’assistance tierces qui diagnostiquent les problèmes liés à l’extension des protocoles 802,11 utilisés par le WiFi natif.</span><span class="sxs-lookup"><span data-stu-id="3bf12-115">The Revised Native Wifi (RNWF) extensible helper class is the parent for third-party helper classes that diagnose issues related to extending 802.11 protocols used by Native Wifi.</span></span>

<span data-ttu-id="3bf12-116">Les deux attributs clés fournis par la classe d’assistance RNWF sont le GUID de l’interface dans laquelle le problème s’est produit et le contexte de connexion.</span><span class="sxs-lookup"><span data-stu-id="3bf12-116">The two key attributes provided by the RNWF helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="3bf12-117">GUID de l’interface : cet attribut est nommé « ID d’interface » et est de type **au \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="3bf12-117">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="3bf12-118">Contexte de connexion : cet attribut est nommé ID réseau et est de type \_ chaîne d’octets \_ .</span><span class="sxs-lookup"><span data-stu-id="3bf12-118">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="3bf12-119">Cette chaîne est en fait une mémoire tampon de la structure de l' \_ \_ ID WLAN WDIAG IHV \_ définie dans Wlanihv. h.</span><span class="sxs-lookup"><span data-stu-id="3bf12-119">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in Wlanihv.h.</span></span> <span data-ttu-id="3bf12-120">Cette structure est définie comme suit.</span><span class="sxs-lookup"><span data-stu-id="3bf12-120">This structure is defined as follows.</span></span>

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
> <span data-ttu-id="3bf12-121">**WDIAG \_ L' \_ indicateur d’ID WLAN IHV \_ \_ \_ \_ activé** pour la sécurité est la seule valeur **dwFlags** possible.</span><span class="sxs-lookup"><span data-stu-id="3bf12-121">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="3bf12-122">L’attribut correspondant pour la classe d’assistance tierce doit être identique à l’ID de service de son module logiciel correspondant.</span><span class="sxs-lookup"><span data-stu-id="3bf12-122">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="3bf12-123">Il s’agit également du même nom que le tiers doit être inscrit dans le registre.</span><span class="sxs-lookup"><span data-stu-id="3bf12-123">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="3bf12-124">Les diagnostics sans fil interrogent l’ID de service pendant la session sans fil dans laquelle le problème s’est produit.</span><span class="sxs-lookup"><span data-stu-id="3bf12-124">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="3bf12-125">Les informations sont retournées à NDF, qui détermine si la classe d’assistance tierce est présente et inscrite, puis l’appelle.</span><span class="sxs-lookup"><span data-stu-id="3bf12-125">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="3bf12-126">Le tableau suivant répertorie les attributs correspondants pour la classe d’assistance extensible RNWF.</span><span class="sxs-lookup"><span data-stu-id="3bf12-126">The following table lists the matching attributes for the RNWF extensible helper class.</span></span>



| <span data-ttu-id="3bf12-127">Nom</span><span class="sxs-lookup"><span data-stu-id="3bf12-127">Name</span></span>          | <span data-ttu-id="3bf12-128">Type</span><span class="sxs-lookup"><span data-stu-id="3bf12-128">Type</span></span>    | <span data-ttu-id="3bf12-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bf12-129">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="3bf12-130">DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="3bf12-130">DiagnosticsID</span></span> | <span data-ttu-id="3bf12-131">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="3bf12-131">REG\_SZ</span></span> | <span data-ttu-id="3bf12-132">\[\_Chaîne GUID \_ DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="3bf12-132">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="l2security-extensible-helper-class"></a><span data-ttu-id="3bf12-133">Classe d’assistance extensible L2Security</span><span class="sxs-lookup"><span data-stu-id="3bf12-133">L2Security Extensible Helper Class</span></span>

<span data-ttu-id="3bf12-134">Nom de la classe d’assistance parente</span><span class="sxs-lookup"><span data-stu-id="3bf12-134">Parent Helper Class Name</span></span>

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

<span data-ttu-id="3bf12-135">La classe d’assistance extensible Layer 2 Security (L2Security) est le parent des classes d’assistance tierces qui diagnostiquent les problèmes liés aux services et modules logiciels correspondants qui remplacent les fonctionnalités de sécurité de couche 2.</span><span class="sxs-lookup"><span data-stu-id="3bf12-135">The Layer 2 Security (L2Security) extensible helper class is the parent for third-party helper classes that diagnose issues related to corresponding services and software modules that replace Layer 2 Security functionality.</span></span>

<span data-ttu-id="3bf12-136">Les deux attributs clés fournis par la classe d’assistance de sécurité de couche 2 sont le GUID de l’interface dans laquelle le problème s’est produit et le contexte de connexion.</span><span class="sxs-lookup"><span data-stu-id="3bf12-136">The two key attributes provided by the Layer 2 Security helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="3bf12-137">GUID de l’interface : cet attribut est nommé « ID d’interface » et est de type **au \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="3bf12-137">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="3bf12-138">Contexte de connexion : cet attribut est nommé ID réseau et est de type \_ chaîne d’octets \_ .</span><span class="sxs-lookup"><span data-stu-id="3bf12-138">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="3bf12-139">Cette chaîne est en fait une mémoire tampon de la structure de l' \_ \_ ID WLAN WDIAG IHV \_ définie dans wlanihv. h.</span><span class="sxs-lookup"><span data-stu-id="3bf12-139">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in wlanihv.h.</span></span> <span data-ttu-id="3bf12-140">Cette structure est définie comme suit.</span><span class="sxs-lookup"><span data-stu-id="3bf12-140">This structure is defined as follows.</span></span>

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
> <span data-ttu-id="3bf12-141">**WDIAG \_ L' \_ indicateur d’ID WLAN IHV \_ \_ \_ \_ activé** pour la sécurité est la seule valeur **dwFlags** possible.</span><span class="sxs-lookup"><span data-stu-id="3bf12-141">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="3bf12-142">L’attribut correspondant pour la classe d’assistance tierce doit être identique à l’ID de service de son module logiciel correspondant.</span><span class="sxs-lookup"><span data-stu-id="3bf12-142">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="3bf12-143">Il s’agit également du même nom que le tiers doit être inscrit dans le registre.</span><span class="sxs-lookup"><span data-stu-id="3bf12-143">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="3bf12-144">Les diagnostics sans fil interrogent l’ID de service pendant la session sans fil dans laquelle le problème s’est produit.</span><span class="sxs-lookup"><span data-stu-id="3bf12-144">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="3bf12-145">Les informations sont retournées à NDF, qui détermine si la classe d’assistance tierce est présente et inscrite, puis l’appelle.</span><span class="sxs-lookup"><span data-stu-id="3bf12-145">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="3bf12-146">Le tableau suivant répertorie les attributs correspondants pour la classe d’assistance extensible de sécurité de couche 2.</span><span class="sxs-lookup"><span data-stu-id="3bf12-146">The following table lists the matching attributes for the Layer 2 Security extensible helper class.</span></span>



| <span data-ttu-id="3bf12-147">Nom</span><span class="sxs-lookup"><span data-stu-id="3bf12-147">Name</span></span>          | <span data-ttu-id="3bf12-148">Type</span><span class="sxs-lookup"><span data-stu-id="3bf12-148">Type</span></span>    | <span data-ttu-id="3bf12-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bf12-149">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="3bf12-150">DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="3bf12-150">DiagnosticsID</span></span> | <span data-ttu-id="3bf12-151">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="3bf12-151">REG\_SZ</span></span> | <span data-ttu-id="3bf12-152">\[\_Chaîne GUID \_ DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="3bf12-152">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="matching-attributes"></a><span data-ttu-id="3bf12-153">Attributs correspondants</span><span class="sxs-lookup"><span data-stu-id="3bf12-153">Matching Attributes</span></span>

<span data-ttu-id="3bf12-154">**DiagnosticsID**</span><span class="sxs-lookup"><span data-stu-id="3bf12-154">**DiagnosticsID**</span></span>

<span data-ttu-id="3bf12-155">802,11 les diagnostics sans fil interrogent le *DiagnosticsID* à partir du service Wi-Fi natif principal afin de déterminer si des extensions ou des modules de sécurité tiers sont installés et impliqués dans la connexion.</span><span class="sxs-lookup"><span data-stu-id="3bf12-155">802.11 Wireless Diagnostics will query the *DiagnosticsID* from the core Native Wifi service in order to find out if any third-party wireless extensions or security modules are installed and involved in the connection.</span></span> <span data-ttu-id="3bf12-156">Les diagnostics sans fil fournissent alors des informations sur ces classes d’assistance tierces à l’aide du *DiagnosticsID* en tant qu’attribut correspondant.</span><span class="sxs-lookup"><span data-stu-id="3bf12-156">Wireless Diagnostics will then provide hypotheses to these third-party helper classes using the *DiagnosticsID* as the matching attribute.</span></span> <span data-ttu-id="3bf12-157">Toutes les classes d’assistance tierces doivent être incluses dans et installées avec le package de pilotes associé.</span><span class="sxs-lookup"><span data-stu-id="3bf12-157">Any third-party helper classes should be included in and installed with the associated driver package.</span></span> <span data-ttu-id="3bf12-158">Le *DiagnosticsID* sera défini dans le fichier INF de miniport comme clé de Registre dans la directive [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3bf12-158">The *DiagnosticsID* will be defined in the miniport INF file as a registry key in the [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) directive.</span></span>

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

<span data-ttu-id="3bf12-159">Cette clé définit l’ID de la classe d’assistance sans fil pour le module de logiciel tiers.</span><span class="sxs-lookup"><span data-stu-id="3bf12-159">This key defines the ID of the wireless helper class for the third-party software module.</span></span> <span data-ttu-id="3bf12-160">Cette clé est facultative pour l’infrastructure d’extensibilité, mais elle est nécessaire si l’implémentation comprend une classe d’assistance sans fil IHV qui se connecte à NDF et peut diagnostiquer les problèmes de connectivité liés aux extensions sans fil ou de sécurité RNWF.</span><span class="sxs-lookup"><span data-stu-id="3bf12-160">This key is optional for the extensibility framework, but it is needed if the implementation includes an IHV Wireless Helper Class that plugs into NDF and can diagnose connectivity problems related to the RNWF wireless or security extensions.</span></span> <span data-ttu-id="3bf12-161">Les classes d’assistance de diagnostic WLAN MS interrogent cet ID à partir du service de configuration automatique sans fil lorsque les modules IHV sont installés et fournissent cet ID en tant que référence ou attribut correspondant à NDF au cours d’une session de diagnostic pour que NDF puisse appeler la classe d’assistance sans fil tierce appropriée lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3bf12-161">MS WLAN diagnostics helper classes will query this ID from the Wireless Auto Configuration Service when IHV modules are installed and will provide this ID as the reference or matching attribute to NDF during a diagnostics session so that NDF can call the appropriate third-party wireless helper class when necessary.</span></span>

<span data-ttu-id="3bf12-162">**\[\_Chaîne GUID \_ DiagnosticsID\]**</span><span class="sxs-lookup"><span data-stu-id="3bf12-162">**\[DiagnosticsID\_GUID\_String\]**</span></span>

<span data-ttu-id="3bf12-163">Cette valeur doit être une chaîne de toutes les lettres majuscules.</span><span class="sxs-lookup"><span data-stu-id="3bf12-163">This value must be a string of all uppercase letters.</span></span> <span data-ttu-id="3bf12-164">Par exemple, « {12345678-9ABC-DEF0-1234-56789ABCDEF0} ».</span><span class="sxs-lookup"><span data-stu-id="3bf12-164">For example, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".</span></span>

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a><span data-ttu-id="3bf12-165">Étendue des classes d’assistance de diagnostic sans fil 802,11</span><span class="sxs-lookup"><span data-stu-id="3bf12-165">Scope of 802.11 Wireless Diagnostics Helper Classes</span></span>

<span data-ttu-id="3bf12-166">les classes d’assistance de diagnostic sans fil 802,11 diagnostiquent actuellement les problèmes de réseau sans fil dans les domaines suivants.</span><span class="sxs-lookup"><span data-stu-id="3bf12-166">802.11 wireless diagnostics helper classes currently diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="3bf12-167">Les problèmes de connectivité 802,11, y compris l’Association 802,11, l’authentification 802,11, les paramètres de sécurité 802,11 relatifs aux normes 802,11 & protocoles pris en charge en mode natif dans le système d’exploitation et les problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="3bf12-167">Any 802.11 connectivity issues including 802.11 association, 802.11 authentication, 802.11 security settings related to 802.11 standards & protocols natively supported in the operating system, and performance issues.</span></span>
-   <span data-ttu-id="3bf12-168">Problèmes de sécurité de couche 2 concernant les configurations 802.1 x et problèmes liés à l’authentification de couche 2 à l’aide de méthodes prises en charge en mode natif sur Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3bf12-168">Layer 2 Security issues with regards to 802.1x configurations and any issues related to layer 2 authentication using methods natively supported on Windows Vista and Windows Server 2008.</span></span>
-   <span data-ttu-id="3bf12-169">Incompatibilité de configuration dans les paramètres de profil entre le client et le point d’accès ou l’infrastructure réseau et les services.</span><span class="sxs-lookup"><span data-stu-id="3bf12-169">Configuration mismatches in profile settings between the client and the Access Point or the network infrastructure and services.</span></span>

<span data-ttu-id="3bf12-170">les classes d’assistance de diagnostic sans fil 802,11 ne diagnostiquent pas actuellement les problèmes de réseau sans fil dans les domaines suivants.</span><span class="sxs-lookup"><span data-stu-id="3bf12-170">802.11 wireless diagnostics helper classes currently do not diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="3bf12-171">Problèmes liés aux extensions 802,11 tierces, y compris les paramètres de profil ou de pilote associés à ces extensions.</span><span class="sxs-lookup"><span data-stu-id="3bf12-171">Issues related to third-party 802.11 extensions including any profile or driver settings related to these extensions.</span></span>
-   <span data-ttu-id="3bf12-172">Problèmes liés aux méthodes EAP tierces.</span><span class="sxs-lookup"><span data-stu-id="3bf12-172">Issues related to third-party EAP methods.</span></span>
-   <span data-ttu-id="3bf12-173">Problèmes liés au pilote miniport sans fil.</span><span class="sxs-lookup"><span data-stu-id="3bf12-173">Wireless miniport driver issues.</span></span>
-   <span data-ttu-id="3bf12-174">Tout protocole de sécurité 802,11 et de couche 2 ou des problèmes liés aux normes qui ne sont pas pris en charge en mode natif.</span><span class="sxs-lookup"><span data-stu-id="3bf12-174">Any 802.11 and layer 2 security protocol or standards-related issues that are not natively supported.</span></span>
-   <span data-ttu-id="3bf12-175">Problèmes au niveau du système ou du composant qui peuvent avoir un impact sur la connectivité sans fil, tels que la gestion de l’alimentation, l’espace disque insuffisant, les conditions de mémoire et les problèmes matériels.</span><span class="sxs-lookup"><span data-stu-id="3bf12-175">System or component-level issues that might impact wireless connectivity, such as power management, low disk space, memory conditions, and hardware problems.</span></span>

<span data-ttu-id="3bf12-176">En outre, 802,11 Diagnostics sans fil n’analyse pas les cas [**utilisation élevée du**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) .</span><span class="sxs-lookup"><span data-stu-id="3bf12-176">Additionally, 802.11 Wireless Diagnostics does not analyze [**HighUtilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) cases.</span></span> <span data-ttu-id="3bf12-177">Les problèmes de performances sans fil identifiés seront analysés et signalés en tant que cas [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) .</span><span class="sxs-lookup"><span data-stu-id="3bf12-177">Identified wireless performance issues will be analyzed and reported as [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) cases.</span></span>

 

 




