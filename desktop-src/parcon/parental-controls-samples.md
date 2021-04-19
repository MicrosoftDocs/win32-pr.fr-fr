---
description: Exemples de contrôle parental
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Exemples de contrôle parental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534690"
---
# <a name="parental-controls-samples"></a>Exemples de contrôle parental

Des exemples de code pour les contrôles parentaux sont disponibles sous chemins d’accès <installation directory> \\ Windows \\ <version number> \\ exemples de \\ sécurité \\ parentalcontrols. Les exemples sont les suivants :

## <a name="utilities"></a>Services

Fonctionnalités d’assistance pour la gestion COM de base, les opérations de chaîne SID et les fonctionnalités de lecture et d’écriture WMI. Tous les autres exemples dépendent de ce projet, sauf indication contraire.

## <a name="complianceapi"></a>ComplianceAPI

Application console pilotée par ligne de commande montrant comment utiliser l’API de compatibilité pour récupérer un sous-ensemble de paramètres de clé pour un utilisateur.

## <a name="complianceapp"></a>ComplianceApp

Application console simple illustrant l’utilisation de l’API de conformité pour vérifier la journalisation requise et les restrictions spécifiques. Si les restrictions de temps sont activées, l’application attend également les événements de déconnexion imminents.

## <a name="uiextensibility"></a>UIExtensibility

Application console pilotée par ligne de commande illustrant l’utilisation des API WMI et du schéma WPC pour répertorier, interroger, ajouter, modifier et supprimer des entrées de lien d’extensibilité de l’interface utilisateur.

Exemple de ligne de commande pour l’exemple :

"D : \\ WPC \\ Samples \\ Security \\ parentalcontrols \\ UIExtensibility \\ Debug \\ UIExtensibility" Add/g : {FD59BB7F-54AB-11DB-9666-00E08161165F}/c : 0/N : D:/WPC/Samples/Security/parentalcontrols/UiExtRC/Debug/UiExtRC.dll,-101/S : D:/WPC/Samples/Security/parentalcontrols/UiExtRC/Debug/UiExtRC.dll,-103/I : d:/WPC/Samples/Security/parentalcontrols/UiExtRC/Debug/UiExtRC.dll,-104/D : d:/WPC/Samples/Security/parentalcontrols/UiExtRC/Debug/UiExtRC.dll,-106/e : c : \\ Windows \\Notepad.exe

où UiExtRC est une DLL de ressource simple avec des ressources de chaîne pour les ID 101 et 103, et 24x24 pixel 32 bits avec des bitmaps alpha pour les ressources 104 et 106.

## <a name="webextensibility"></a>Extensibilité

Application console pilotée par ligne de commande montrant comment utiliser les API WMI et le schéma WPC pour répertorier, ajouter et supprimer des entrées d’exemption d’URL ou d’application HTTP, et pour définir et réinitialiser un remplacement de filtre de contenu Web avec les propriétés FilterID et FilterName.

L’accès aux listes d’exemptions d’URL et d’applications HTTP en lecture seule n’est pas affiché, mais le code permettant de lire les listes est le même que pour le cas de lecture/écriture, à l’exception de la modification du paramètre WMI.

 

 



