---
description: .
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Suppression de Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836b2f447735c8e3595955ca7e99f1ae818c3d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210229"
---
# <a name="removal-of-windows-mail"></a>Suppression de Windows Mail

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**Serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -haute  
**Fréquence** -élevée  









## <a name="description"></a>Description

Microsoft déprécie l’utilitaire de messagerie Windows et désactive l’API CoStartOutlookExpress. Les autres API de messagerie ont été marquées comme dépréciées et sont susceptibles d’être supprimées dans une version ultérieure de Windows. Toutefois, les API documentées publiquement qui ne sont pas marquées comme dépréciées ou obsolètes continuent de fonctionner dans Windows 7. Les binaires restent sur les systèmes des utilisateurs et continuent à être accessibles via les API, en particulier dans les cas mentionnés ci-dessus. En outre, les fichiers de courrier électronique (. eml) et les fichiers de News (. NWS) des utilisateurs resteront sur le système.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

La suppression des résultats Windows Mail est due à ce qui suit :

-   Tous les points d’entrée vers Windows Mail et contacts (par exemple, le menu Démarrer, les raccourcis créés par l’utilisateur, l’exécution de démarrage >, etc.) sont supprimés ou désactivés. Certaines d’entre elles sont complètement supprimées, d’autres échouent lors de la tentative de lancement.
-   Toutes les dll sont expédiées dans la zone
-   Les API documentées publiquement continuent de fonctionner comme dans Windows Vista
-   Toutes les API qui tentent de lancer l’interface utilisateur principale du navigateur ont été modifiées pour créer une défaillance silencieuse. La fonction retourne Success, mais n’affiche pas l’interface utilisateur pour l’utilisateur. Les API qui appellent d’autres boîtes de dialogue (par exemple, le spouleur ou la boîte de dialogue comptes) continuent à afficher cette interface utilisateur.
-   Les gestionnaires de protocole (mailto, LDAP, News, SNEWS, NNTP) ne sont pas associés à Windows Mail ou aux contacts. Lorsque vous tentez de les lancer, les clients voient une boîte de dialogue d’erreur qui les pointe vers l’emplacement où ils peuvent définir ces associations sur un autre programme.
-   Les associations de fichiers (. eml,. NWS,. contact,. Group,. wab,. P7C,. VFC) sont interrompues ou désactivées. Lorsque vous tentez d’ouvrir un fichier avec ces extensions, les clients obtiennent une boîte de dialogue leur proposant d’autres applications installées qu’ils peuvent utiliser et les pointant vers une page Web proposant des solutions
-   Tout fichier utilisateur (par exemple, les fichiers ou les messages de contact) reste sur le système dans le scénario de mise à niveau
-   Le dossier contacts est masqué par défaut afin que les clients ne le voient pas
-   Les API sont marquées comme dépréciées dans MSDN
-   La fonction d’aperçu de fichier est supprimée
-   Les hooks de l’interpréteur de commandes dans le menu contextuel sont supprimés
-   La fonction de recherche de fichiers est supprimée

## <a name="mitigation"></a>Limitation des risques

Les utilisateurs doivent installer Windows Live Mail ou tout autre produit de messagerie capable de lire les fichiers. eml et. NWS.

## <a name="solution"></a>Solution

Détecte si un gestionnaire de messagerie par défaut est installé. Si ce n’est pas le cas, conseillez à l’utilisateur d’installer Windows Live Mail ou tout autre produit capable de lire les fichiers. eml et. NWS.

Ne concevez pas le code qui appelle l’API d’interface utilisateur de Windows Mail, car il ne fonctionnera pas. Vous devez trouver d’autres façons d’accéder aux fichiers. eml et. NWS. En outre, dès que possible, interrompez votre confiance sur toutes les autres API Windows Mail.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilité, performances, fiabilité et test d’utilisabilité

-   Exercez votre application dans un environnement Windows 7 pour vous assurer que l’application n’essaie pas d’appeler l’API d’interface utilisateur.
-   Vous pouvez également exécuter Application Compatibility Toolkit (ACT) à l’aide de l’évaluateur de compatibilité Windows (WCE) pour localiser les problèmes potentiels en raison de l’obsolescence de cette fonctionnalité.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

<dl>

[Téléchargement de l’outil Application Compatibility Toolkit](/windows-hardware/get-started/adk-install)  
</dl>

 

 
