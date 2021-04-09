---
description: Schéma de profil haut débit mobile v3.
ms.assetid: f7a3598f-57dd-4178-896f-31b4d2f65e56
title: Schéma de profil haut débit mobile v3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea42c0c4b6384b85e5373d6537f52cf8c9499e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862509"
---
# <a name="mobile-broadband-profile-schema-v3"></a><span data-ttu-id="a5f55-103">Schéma de profil haut débit mobile v3</span><span class="sxs-lookup"><span data-stu-id="a5f55-103">Mobile Broadband Profile Schema v3</span></span>

<span data-ttu-id="a5f55-104">Le schéma de profil large bande 8Mobile Windows v3 est disponible dans l’espace de noms `https://www.microsoft.com/networking/WWAN/profile/v3` .</span><span class="sxs-lookup"><span data-stu-id="a5f55-104">The Windows 8Mobile Broadband Profile Schema v3 is available in the namespace `https://www.microsoft.com/networking/WWAN/profile/v3`.</span></span>

-   [<span data-ttu-id="a5f55-105">Éléments du schéma de profil haut débit mobile v3</span><span class="sxs-lookup"><span data-stu-id="a5f55-105">Mobile Broadband Profile Schema v3 Elements</span></span>](mobile-broadband-profile-schema-v3-elements.md)

``` syntax
<xs:schema targetNamespace="https://www.microsoft.com/networking/WWAN/profile/v3" 
    xmlns="https://www.microsoft.com/networking/WWAN/profile/v3"  
    xmlns:xs="https://www.w3.org/2001/XMLSchema" 
    xmlns:WWAN_profile_v2="https://www.microsoft.com/networking/WWAN/profile/v2"  
    elementFormDefault="qualified"> 

    <xs:import namespace="https://www.microsoft.com/networking/WWAN/profile/v2" schemaLocation="WWAN_profile_v2.xsd"/> 

    <!-- Flag to indicate whether this is an additional PDP context profile, default is "false" --> 
    <xs:element name="IsAdditionalPdpContextProfile" type="xs:boolean"/> 
</xs:schema> 
```

 

 



