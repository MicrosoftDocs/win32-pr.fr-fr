---
title: Configuration du serveur pour les téléchargements
description: Pour télécharger des fichiers sur un serveur à l’aide de BITS, IIS et l’extension ISAPI du serveur BITS doivent être installés sur le serveur. Pour connaître la configuration requise pour IIS, consultez configuration IIS requise pour les téléchargements BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e075478f6e0335c6bf601a9289d93d4d3fac2aefd9e4f1ef820e938a1bfc0ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004719"
---
# <a name="setting-up-the-server-for-uploads"></a>Configuration du serveur pour les téléchargements

Pour télécharger des fichiers sur un serveur à l’aide de BITS, IIS et l’extension ISAPI du serveur BITS doivent être installés sur le serveur. Pour connaître la configuration requise pour IIS, consultez [configuration IIS requise pour les téléchargements bits](iis-requirements-for-bits-uploads.md).

Pour plus d’informations sur la configuration du répertoire virtuel IIS utilisé par BITS pour les téléchargements, consultez les rubriques suivantes.

-   [Définition des autorisations sur les répertoires virtuels](setting-permissions-on-virtual-directories.md)
-   [Écriture d’un script pour configurer le répertoire virtuel](writing-a-script-to-configure-the-virtual-directory.md)
-   [Utilisation de l’interface utilisateur IIS pour configurer le répertoire virtuel](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [Empêcher plusieurs chargements](preventing-multiple-uploads.md)
-   [Télécharger Meilleures pratiques](upload-best-practices.md)

> [!Note]  
> Certaines installations IIS incluent le composant de filtrage UrlScan. Si UrlScan est activé, l’administrateur doit ajouter le verbe « BITS \_ auto » à la liste des verbes HTTP autorisés d’URLScan. Dans le cas contraire, les téléchargements du client BITS échoueront. Pour plus d’informations sur l’activation des verbes dans UrlScan, consultez la documentation d’UrlScan.

 

 

 




