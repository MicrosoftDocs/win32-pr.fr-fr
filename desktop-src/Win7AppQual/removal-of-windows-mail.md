---
description: suppression de la messagerie Windows
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: suppression de la messagerie Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2456fa5bdf9d981385f2b4832250358f7bfdab1b223aeb3658d8df4cc212237b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328933"
---
# <a name="removal-of-windows-mail"></a>suppression de la messagerie Windows

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -haute  
**Fréquence** -élevée  









## <a name="description"></a>Description

Microsoft déprécie l’utilitaire de messagerie Windows et désactive l’API CoStartOutlookExpress. les autres api de messagerie ont été marquées comme dépréciées et sont susceptibles d’être supprimées dans une version ultérieure de Windows. toutefois, les api documentées publiquement qui ne sont pas marquées comme dépréciées ou obsolètes continuent de fonctionner dans Windows 7. Les binaires restent sur les systèmes des utilisateurs et continuent à être accessibles via les API, en particulier dans les cas mentionnés ci-dessus. En outre, les fichiers de courrier électronique (. eml) et les fichiers de News (. NWS) des utilisateurs resteront sur le système.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

la suppression de Windows message est due à ce qui suit :

-   tous les points d’entrée pour Windows le courrier électronique et les Contacts (par exemple, le Menu démarrer, les raccourcis créés par l’utilisateur, l’exécution de démarrage >, etc.) sont supprimés ou désactivés. Certaines d’entre elles sont complètement supprimées, d’autres échouent lors de la tentative de lancement.
-   Toutes les dll sont expédiées dans la zone
-   les api documentées publiquement continuent de fonctionner comme dans Windows Vista
-   Toutes les API qui tentent de lancer l’interface utilisateur principale du navigateur ont été modifiées pour créer une défaillance silencieuse. La fonction retourne Success, mais n’affiche pas l’interface utilisateur pour l’utilisateur. Les API qui appellent d’autres boîtes de dialogue (par exemple, le spouleur ou la boîte de dialogue comptes) continuent à afficher cette interface utilisateur.
-   les gestionnaires de protocole (mailto, ldap, news, snews, nntp) ne sont pas associés à des messages ou à des Contacts Windows. Lorsque vous tentez de les lancer, les clients voient une boîte de dialogue d’erreur qui les pointe vers l’emplacement où ils peuvent définir ces associations sur un autre programme.
-   Les associations de fichiers (. eml,. NWS,. contact,. Group,. wab,. P7C,. VFC) sont interrompues ou désactivées. Lorsque vous tentez d’ouvrir un fichier avec ces extensions, les clients obtiennent une boîte de dialogue leur proposant d’autres applications installées qu’ils peuvent utiliser et les pointant vers une page Web proposant des solutions
-   Tout fichier utilisateur (par exemple, les fichiers ou les messages de contact) reste sur le système dans le scénario de mise à niveau
-   Le dossier contacts est masqué par défaut afin que les clients ne le voient pas
-   Les API sont marquées comme dépréciées dans MSDN
-   La fonction d’aperçu de fichier est supprimée
-   Les hooks de l’interpréteur de commandes dans le menu contextuel sont supprimés
-   La fonction de recherche de fichiers est supprimée

## <a name="mitigation"></a>Limitation des risques

les utilisateurs doivent installer Windows Live Mail ou tout autre produit de messagerie capable de lire les fichiers. eml et. nws.

## <a name="solution"></a>Solution

Détecte si un gestionnaire de messagerie par défaut est installé. si ce n’est pas le cas, conseillez à l’utilisateur d’installer Windows Live Mail ou tout autre produit capable de lire les fichiers. eml et. nws.

ne concevez pas le code qui appelle l’API d’interface utilisateur Windows Mail, car il ne fonctionnera pas. Vous devez trouver d’autres façons d’accéder aux fichiers. eml et. NWS. en outre, dès que possible, interrompez votre confiance sur toutes les autres api de messagerie Windows.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilité, performances, fiabilité et test d’utilisabilité

-   exercez votre application dans un environnement Windows 7 pour vous assurer que l’application n’essaie pas d’appeler l’API d’interface utilisateur.
-   vous pouvez également exécuter le Shared Computer Toolkit de compatibilité des applications (ACT) à l’aide du Windows Compatibility Evaluator (WCE) pour localiser les problèmes potentiels en raison de l’obsolescence de cette fonctionnalité.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

<dl>

[compatibilité des applications Shared Computer Toolkit téléchargement](/windows-hardware/get-started/adk-install)  
</dl>

 

 
