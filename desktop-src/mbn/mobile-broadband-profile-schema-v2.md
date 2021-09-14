---
description: Schéma de profil de haut débit mobile v2.
ms.assetid: 0E140DCC-373C-44B3-8A91-F38AE7A5797C
title: Schéma de profil haut débit mobile v2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1328e2b108c80addc8f69584cd1b3cbd797ac777
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415864"
---
# <a name="mobile-broadband-profile-schema-v2"></a>Schéma de profil haut débit mobile v2

le schéma de profil large bande Windows 8Mobile v2 est disponible dans l’espace de noms `https://www.microsoft.com/networking/WWAN/profile/v2` .

-   [Éléments du schéma de profil haut débit mobile v2](mobile-broadband-profile-schema-v2-elements.md)

``` syntax
<xs:schema targetNamespace="https://www.microsoft.com/networking/WWAN/profile/v2"
    xmlns="https://www.microsoft.com/networking/WWAN/profile/v2" 
    xmlns:xs="https://www.w3.org/2001/XMLSchema"
    xmlns:WWAN_profile_v1="https://www.microsoft.com/networking/WWAN/profile/v1" 
    elementFormDefault="qualified">

    <xs:import namespace="https://www.microsoft.com/networking/WWAN/profile/v1" schemaLocation="WWAN_profile_v1.xsd"/>

    <!-- Flag to indicate whether this is a purchase profile, default is "false" -->
    <xs:element name="IsPurchaseProfile" type="xs:boolean"/>

    <!-- Display Provider Name -->
    <xs:element name="DisplayProviderName" type="WWAN_profile_v1:providerNameType"/>

</xs:schema>
```

 

 



