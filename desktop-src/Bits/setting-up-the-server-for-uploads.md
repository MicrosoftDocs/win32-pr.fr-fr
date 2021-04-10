---
title: Configuration du serveur pour les téléchargements
description: Pour télécharger des fichiers sur un serveur à l’aide de BITS, IIS et l’extension ISAPI du serveur BITS doivent être installés sur le serveur. Pour connaître la configuration requise pour IIS, consultez configuration IIS requise pour les téléchargements BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190795"
---
# <a name="setting-up-the-server-for-uploads"></a>Configuration du serveur pour les téléchargements

Pour télécharger des fichiers sur un serveur à l’aide de BITS, IIS et l’extension ISAPI du serveur BITS doivent être installés sur le serveur. Pour connaître la configuration requise pour IIS, consultez [configuration IIS requise pour les téléchargements bits](iis-requirements-for-bits-uploads.md).

Pour plus d’informations sur la configuration du répertoire virtuel IIS utilisé par BITS pour les téléchargements, consultez les rubriques suivantes.

-   [Définition des autorisations sur les répertoires virtuels](setting-permissions-on-virtual-directories.md)
-   [Écriture d’un script pour configurer le répertoire virtuel](writing-a-script-to-configure-the-virtual-directory.md)
-   [Utilisation de l’interface utilisateur IIS pour configurer le répertoire virtuel](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [Empêcher plusieurs chargements](preventing-multiple-uploads.md)
-   [Télécharger les meilleures pratiques](upload-best-practices.md)

> [!Note]  
> Certaines installations IIS incluent le composant de filtrage UrlScan. Si UrlScan est activé, l’administrateur doit ajouter le verbe « BITS \_ auto » à la liste des verbes HTTP autorisés d’URLScan. Dans le cas contraire, les téléchargements du client BITS échoueront. Pour plus d’informations sur l’activation des verbes dans UrlScan, consultez la documentation d’UrlScan.

 

 

 




