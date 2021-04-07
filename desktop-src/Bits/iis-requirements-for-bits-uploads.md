---
title: Configuration requise pour IIS pour les téléchargements BITS
description: Pour les téléchargements, BITS requiert IIS 6,0 sur Windows Server 2003 et IIS 7,0 sur Windows Server 2008 ; BITS ne prend pas en charge IIS 5,1 sur Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671613"
---
# <a name="iis-requirements-for-bits-uploads"></a>Configuration requise pour IIS pour les téléchargements BITS

Pour les téléchargements, BITS requiert IIS 6,0 sur Windows Server 2003 et IIS 7,0 sur Windows Server 2008 ; BITS ne prend pas en charge IIS 5,1 sur Windows XP. Le répertoire virtuel IIS doit être activé pour les téléchargements et les extensions IIS BITS doivent être configurées.

**Installations principales de Windows Server :** Les extensions IIS BITS ne sont pas prises en charge.

Sur Windows Server 2008, utilisez la **Gestionnaire de serveur** pour installer la fonctionnalité extensions du serveur bits. Dans **Gestionnaire de serveur**, cliquez sur **fonctionnalités** dans le volet gauche. Dans l' **Assistant Ajout de fonctionnalités**, activez les extensions du serveur bits. Notez que les rôles de compatibilité avec la gestion IIS 6 doivent être installés.

Sur Windows Server 2003, utilisez l' **Assistant Composants Windows** pour installer l’extension de serveur bits. Dans **le panneau de configuration**, sélectionnez **Ajout/suppression de programmes**. Ensuite, sélectionnez **Ajouter/supprimer des composants Windows** pour afficher l **'Assistant composants de Windows**. L’extension du serveur BITS est un sous-composant de Internet Information Services (IIS) qui est un sous-composant du serveur d’applications Web.

> [!Note]  
> Si le service IISAdmin est redémarré, le processus de travail IIS doit être recyclé pour que le service BITS puisse reprendre les téléchargements. Le processus de travail IIS peut être recyclé manuellement à l’aide de l’utilitaire de ligne de commande **IISReset.exe** .

 

Pour plus d’informations sur la configuration d’IIS pour les chargements, consultez [configuration du serveur pour les téléchargements](setting-up-the-server-for-uploads.md).

Pour plus d’informations sur les propriétés que BITS ajoute à IIS, consultez [paramètres du serveur bits pour les travaux de téléchargement](bits-server-settings-for-upload-jobs.md).

 

 




