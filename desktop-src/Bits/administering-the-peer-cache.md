---
title: Administration du cache d’homologue
description: Remarque à compter de Windows 7, le modèle de mise en cache d’homologue Service de transfert intelligent en arrière-plan (BITS) 3,0 est déconseillé.
ms.assetid: a33a43e5-02f9-4902-ad3a-ec65b0d80520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b3ea1dd19c9aca855ffd73e174dcb3b588a54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671782"
---
# <a name="administering-the-peer-cache"></a>Administration du cache d’homologue

> [!Note]  
> À compter de Windows 7, le modèle de mise en cache d’homologue Service de transfert intelligent en arrière-plan (BITS) 3,0 est déconseillé. Si BITS 4,0 est installé, le modèle de mise en cache d’homologue BITS 3,0 n’est pas disponible.

 

Pour améliorer les performances de téléchargement, BITS vous permet de télécharger du contenu à partir d’ordinateurs homologues. Pour activer cette fonctionnalité, l’administrateur doit activer le paramètre de stratégie de groupe EnablePeerCaching. S’il est activé, l’homologue peut télécharger du contenu à partir de pairs et servir du contenu à des homologues. L’administrateur peut également utiliser les paramètres de stratégie DisablePeerCachingClient et DisablePeerCachingServer pour empêcher le téléchargement de contenu à partir d’un homologue ou la fourniture de contenu à des homologues, respectivement.

Si les paramètres de stratégie de groupe ne sont pas configurés, une application peut appeler la méthode [**IBitsPeerCacheAdministration :: SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) pour définir la préférence de mise en cache d’homologue pour l’ordinateur. Notez que ces préférences sont remplacées par les paramètres de stratégie de groupe, si elles sont définies ultérieurement. Pour déterminer si l’ordinateur active la mise en cache d’homologue, appelez la méthode [**IBitsPeerCacheAdministration :: GetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-getconfigurationflags) .

Si la mise en cache d’homologue est activée, le service BITS met uniquement en cache le contenu d’un travail si ce travail autorise explicitement son contenu à être mis en cache. En outre, BITS télécharge le contenu à partir d’un homologue si le travail l’autorise explicitement. Pour activer la mise en cache d’homologue pour un travail, appelez la méthode [**IBackgroundCopyJob4 :: SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) .

Outre l’utilisation de stratégie de groupe ou de l’interface [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) pour activer la mise en cache d’homologue, vous pouvez également utiliser l’une ou l’autre méthode pour modifier la taille de cache par défaut et la durée pendant laquelle un fichier non accédé reste dans le cache. Pour modifier les valeurs par défaut à l’aide de l’interface **IBitsPeerCacheAdministration** , appelez les méthodes [**SetMaximumCacheSize**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcachesize) et [**SetMaximumContentAge**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcontentage) . Étant donné que ces méthodes définissent les paramètres de préférence, elles sont remplacées par les paramètres de stratégie de groupe.

Pour répertorier les homologues à partir desquels BITS tente de télécharger du contenu, appelez la méthode [**IBitsPeerCacheAdministration :: EnumPeers**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumpeers) .

Pour répertorier les fichiers dans le cache que BITS servira aux homologues, appelez la méthode [**IBitsPeerCacheAdministration :: EnumRecords**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords) .

Vous ne devez jamais avoir à gérer le cache d’homologue en ce qui concerne la découverte d’homologues ou la suppression d’enregistrements de cache. Cette fonctionnalité a été incluse dans l’interface [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) à des fins d’exhaustivité.

 

 




