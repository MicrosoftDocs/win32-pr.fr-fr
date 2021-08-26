---
title: Configuration requise pour IIS pour les téléchargements BITS
description: pour les téléchargements, BITS requiert iis 6,0 sur Windows server 2003 et iis 7,0 sur Windows server 2008 ; BITS ne prend pas en charge IIS 5,1 sur Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb09ec8c55cce592baf48b4b39faf031e5d6c98909927c0e597be6aaae8712e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004989"
---
# <a name="iis-requirements-for-bits-uploads"></a>Configuration requise pour IIS pour les téléchargements BITS

pour les téléchargements, BITS requiert iis 6,0 sur Windows server 2003 et iis 7,0 sur Windows server 2008 ; BITS ne prend pas en charge IIS 5,1 sur Windows XP. Le répertoire virtuel IIS doit être activé pour les téléchargements et les extensions IIS BITS doivent être configurées.

**installations principales de Windows Server :** Les extensions IIS BITS ne sont pas prises en charge.

sur Windows Server 2008, utilisez la **Gestionnaire de serveur** pour installer la fonctionnalité Extensions du serveur BITS. Dans **Gestionnaire de serveur**, cliquez sur **fonctionnalités** dans le volet gauche. Dans l' **Assistant Ajout de fonctionnalités**, activez les extensions du serveur bits. Notez que les rôles de compatibilité avec la gestion IIS 6 doivent être installés.

sur Windows Server 2003, utilisez l' **assistant composants de Windows** pour installer l’extension du serveur BITS. Dans **le panneau de configuration**, sélectionnez **Ajout/suppression de programmes**. ensuite, sélectionnez **ajouter/supprimer des composants Windows** pour afficher l' **assistant Windows composants**. l’extension du serveur BITS est un sous-composant de Internet Information Services (IIS) qui est un sous-composant du serveur d’applications Web.

> [!Note]  
> Si le service IISAdmin est redémarré, le processus de travail IIS doit être recyclé pour que le service BITS puisse reprendre les téléchargements. Le processus de travail IIS peut être recyclé manuellement à l’aide de l’utilitaire de ligne de commande **IISReset.exe** .

 

Pour plus d’informations sur la configuration d’IIS pour les chargements, consultez [configuration du serveur pour les téléchargements](setting-up-the-server-for-uploads.md).

pour plus d’informations sur les propriétés que BITS ajoute à IIS, consultez [Paramètres du serveur bits pour les tâches de Télécharger](bits-server-settings-for-upload-jobs.md).

 

 




