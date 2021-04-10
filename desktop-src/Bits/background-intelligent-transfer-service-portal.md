---
title: Service de transfert intelligent en arrière-plan (BITS)
description: Le service de transfert intelligent en arrière-plan (BITS) transfère des fichiers (téléchargement ou chargement) entre un client et un serveur et fournit des informations d’avancement liées aux transferts.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Service de transfert intelligent en arrière-plan (BITS)
- Service de transfert intelligent en arrière-plan, page de démarrage
- BITS (voir Service de transfert intelligent en arrière-plan)
- Téléchargement des fichiers BITS
- BITS de transfert de fichiers en arrière-plan
- Téléchargement des fichiers BITS
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: a531821665490735b391ab2714f5b37146c6bc1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941238"
---
# <a name="background-intelligent-transfer-service"></a>Service de transfert intelligent en arrière-plan (BITS)

## <a name="purpose"></a>Objectif

Service de transfert intelligent en arrière-plan (BITS) est utilisé par les programmeurs et les administrateurs système pour télécharger des fichiers depuis ou vers des serveurs Web HTTP et des partages de fichiers SMB. Le service BITS prend en compte le coût du transfert, ainsi que l’utilisation du réseau afin que le travail de premier plan de l’utilisateur ait le moins d’impact possible. BITS gère également les interuptions réseau, en suspendant et en reprenant automatiquement les transferts, même après un redémarrage. Le service BITS comprend des applets de commande PowerShell pour la création et la gestion des transferts, ainsi que l’utilitaire de ligne de commande BitsAdmin.

> [!Note]  
> Le service BITS peut être utilisé par Windows pour télécharger les mises à jour sur votre système local. Si vous êtes un utilisateur final qui recherche des moyens de résoudre les problèmes liés à l’installation de BITS, consultez [résoudre les problèmes de Windows Update](https://support.microsoft.com/help/10164/fix-windows-update-errors). 
 

## <a name="where-applicable"></a>Le cas échéant

Utilisez le service BITS pour les applications qui doivent :

-   Télécharger à partir de ou télécharger des fichiers sur un serveur Web HTTP ou REST ou un serveur de fichiers SMB.
-   Reprendre automatiquement les transferts de fichiers après la déconnexion du réseau et le redémarrage de l’ordinateur.
-   Préserver la réactivité des autres applications réseau.
-   Gardez à l’esprit le coût du réseau, par exemple, les réseaux itinérants
-   Utiliser éventuellement [BranchCache](/windows-server/networking/branchcache/branchcache) pour optimiser le trafic du réseau étendu (WAN)

## <a name="developer-audience"></a>Développeurs concernés

BITS est une interface COM conçue pour les développeurs C et C++ qui peut également être utilisée par les développeurs .NET. Les développeurs UWP doivent utiliser l’API [Windows. Networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) et non l’API bits.

## <a name="bits-versions"></a>Versions de BITS

Pour obtenir l’historique des versions et des informations sur les systèmes d’exploitation antérieurs, consultez [Nouveautés](what-s-new.md).


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                           | Description                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos du service BITS](about-bits.md)<br/>                         | Informations générales sur le service BITS.<br/>                                                                                                                                      |
| [Utilisation de BITS](using-bits.md)<br/>                         | Guide de procédures pour le développement de clients BITS qui transfèrent des fichiers entre un client et un serveur.<br/>                                                                        |
| [Informations de référence sur BITS](bits-reference.md)<br/>                 | Informations de référence pour les interfaces de programmation BITS. Contient également des informations sur les exemples, les outils, les paramètres de serveur pour les travaux de chargement et le protocole de téléchargement.<br/> |
| [Bonnes pratiques](best-practices-when-using-bits.md)<br/> | Informations à prendre en compte lors de la conception d’une application qui utilise BITS.<br/>                                                                                                |



 

## <a name="additional-resources"></a>Ressources supplémentaires

Vous trouverez ci-dessous des ressources supplémentaires.


|             |                                                                                                                                                 |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL de référence .NET   | Pour plus d’informations sur l’utilisation de BITS à partir de .NET à l’aide de dll de référence, consultez [appel de bits à partir de .net avec des dll de référence](/windows/desktop/Bits/bits-dot-net)      |
| Wrapper .NET   | Pour les autres wrappers .NET pour BITS, vous pouvez rechercher [NuGet](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) pour les projets marqués avec la balise bits.        |



 

 

