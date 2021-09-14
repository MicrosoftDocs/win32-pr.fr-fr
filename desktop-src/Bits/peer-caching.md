---
title: Mise en cache d’homologue
description: à partir de Service de transfert intelligent en arrière-plan (bits) 4,0, le Service BITS a été étendu pour autoriser la mise en cache d’homologue au niveau du sous-réseau pour les données d’URL téléchargées à l’aide de Windows BranchCache.
ms.assetid: 4197eed3-1812-4440-99e7-9462635ef6ad
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 3c87e6013bb37610e934c13414bd2636407108ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234317"
---
# <a name="peer-caching"></a>Mise en cache d’homologue

à partir de Service de transfert intelligent en arrière-plan (bits) 4,0, le Service BITS a été étendu pour autoriser la mise en cache d’homologue au niveau du sous-réseau pour les données d’URL téléchargées à l’aide de Windows BranchCache. Les clients BITS peuvent récupérer des données à partir d’autres ordinateurs dans leur propre sous-réseau qui ont déjà téléchargé les données, au lieu de récupérer les données à partir de serveurs distants. pour plus d’informations sur Windows branchcache, voir [vue d’ensemble de branchcache](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).

si un administrateur active Windows BranchCache sur les ordinateurs clients et serveurs d’une organisation via une stratégie de groupe ou des paramètres de configuration locale, BITS utilise Windows BranchCache pour les transferts de données.

-   [Configuration de la mise en cache d’homologue BITS 4,0](#configuration-for-bits-40-peer-caching)
-   [désactivation de Windows BranchCache](#disabling-windows-branchcache)
-   [Vérification et surveillance](#verification-and-monitoring)
-   [Mise en cache d’homologue en BITS 3,0](#peer-caching-in-bits-30)

## <a name="configuration-for-bits-40-peer-caching"></a>Configuration de la mise en cache d’homologue BITS 4,0

La configuration suivante est requise pour que la mise en cache d’homologue en BITS 4,0 fonctionne :

-   Windows BranchCache doit être activé sur le client via une stratégie de groupe ou des paramètres de configuration locaux. Pour plus d’informations, consultez [configuration du client BranchCache](/previous-versions/windows/it-pro/windows-7/dd637820(v=ws.10)).
    > [!Note]  
    > la fonctionnalité Windows BranchCache est désactivée par défaut.

     

-   la fonctionnalité Windows BranchCache est un composant facultatif qui doit être installé sur le serveur. Pour plus d’informations, consultez [configuration du serveur BranchCache](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).
-   le serveur doit également activer la fonctionnalité Windows BranchCache via la stratégie de groupe ou les paramètres de configuration locaux. Pour plus d’informations, consultez [configuration du serveur BranchCache](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).
    > [!Note]  
    > la fonctionnalité Windows BranchCache est désactivée par défaut.

     

La stratégie de groupe BITS par défaut autorise la mise en cache d’homologue. si Windows BranchCache est activé globalement sur un ordinateur, cette fonctionnalité est également activée pour les tâches de transfert BITS. Pour plus d’informations sur les stratégies de groupe spécifiques à BITS, consultez [stratégies de groupe](group-policies.md).

## <a name="disabling-windows-branchcache"></a>désactivation de Windows BranchCache

un administrateur peut utiliser une stratégie de groupe pour désactiver l’utilisation du Windows BranchCache. (Consultez [stratégies de groupe](group-policies.md).) si la Windows BranchCache est désactivée, les clients BITS récupèrent les données uniquement à partir des serveurs distants.

une application peut également désactiver le Windows BranchCache par travail en appelant la méthode [**IBackgroundCopyJob4 :: SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) et en définissant l’indicateur **de \_ \_ \_ CACHE de branche de désactivation BG** .

> [!Note]  
> ces paramètres n’affectent pas l’utilisation de Windows BranchCache par les applications autres que BITS. Ces paramètres ne s’appliquent pas aux transferts BITS sur SMB. BITS ne contrôle aucun paramètre pour Windows les transferts BranchCache sur SMB.

 

## <a name="verification-and-monitoring"></a>Vérification et surveillance

Il existe plusieurs façons de vérifier et surveiller les statistiques de mise en cache d’homologue. Les administrateurs peuvent appeler la méthode [**IBackgroundCopyFile4 :: GetPeerDownloadStats**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibackgroundcopyfile4-getpeerdownloadstats) pour interroger la quantité de données téléchargées à partir des homologues et des serveurs d’origine. Les administrateurs peuvent également consulter le journal des événements pour obtenir l' [ID d’événement 60](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc734635(v=ws.10)), qui fournit des informations spécifiques au travail.

la fonctionnalité Windows BranchCache fournit également un certain nombre de mécanismes pour vérifier et surveiller les statistiques de mise en cache d’homologue. Pour plus d’informations, consultez [vérification et surveillance](/previous-versions/windows/it-pro/windows-7/dd637782(v=ws.10)) et [compteurs de performances](/previous-versions/windows/it-pro/windows-7/dd637826(v=ws.10)).

le modèle de mise en cache d’homologue qui utilise Windows BranchCache remplace le modèle de mise en cache d’homologue utilisé dans BITS 3,0. pour plus d’informations sur Windows BranchCache, consultez les rubriques suivantes :

-   [BranchCache](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj127252(v=ws.11))
-   [Vue d’ensemble de BranchCache](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))
-   [Windows 7 Services](../win7devguide/services.md)
-   [API de distribution d’homologue](../p2psdk/peer-distribution.md)

## <a name="peer-caching-in-bits-30"></a>Mise en cache d’homologue en BITS 3,0

> [!Note]  
> à partir de Windows 7, le modèle de mise en cache d’homologue BITS 3,0 est déconseillé. Si BITS 4,0 est installé, le modèle de mise en cache d’homologue BITS 3,0 n’est pas disponible.

 

Si l’administrateur Active la mise en cache d’homologue et que la tâche autorise le téléchargement de contenu à partir d’un homologue, le service BITS tente de télécharger le contenu à partir d’un ou de plusieurs pairs. Le téléchargement à partir d’un homologue est beaucoup plus rapide que le téléchargement de contenu à partir d’Internet. La mise en cache d’homologue est désactivée par défaut et les travaux doivent autoriser explicitement le téléchargement de contenu à partir d’homologues. Un administrateur peut utiliser une stratégie de groupe pour activer la mise en cache d’homologue. Après l’activation de la mise en cache d’homologue, l’administrateur peut désactiver le téléchargement à partir d’un homologue ou fournir du contenu à un homologue.

Une application peut également activer la mise en cache d’homologue en appelant la méthode [**IBitsPeerCacheAdministration :: SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) . Toutefois, ces paramètres sont remplacés par les paramètres de stratégie de groupe, s’ils sont définis.

Lorsque la mise en cache d’homologue est activée, le service BITS crée une liste d’homologues qui se trouvent dans le même sous-réseau et qui appartiennent au même domaine. La liste n’inclut pas les homologues d’un domaine approuvé. La mise en cache d’homologue ne peut être activée que dans un environnement de domaine.

Le service BITS Découvre les homologues en procédant comme suit :

-   Écoute des serveurs homologues qui s’annoncent eux-mêmes. Un serveur homologue s’annonce lorsqu’il démarre. Le service BITS ajoute le serveur homologue à la liste si le client a besoin de plus de pairs dans sa liste.
-   Diffusion d’une demande de serveurs homologues lorsqu’il a besoin de plus de pairs dans sa liste d’homologues. Les serveurs homologues qui sont disponibles pour traiter le contenu répondent à la demande.

BITS supprime les serveurs homologues de la liste d’homologues si le serveur effectue les opérations suivantes :

-   Échec de l’authentification
-   Est hors connexion (non disponible) pendant trop longtemps
-   Fournit un certificat avec des erreurs

Lorsqu’un travail demande du contenu à partir d’un homologue, BITS choisit de façon aléatoire un sous-ensemble d’homologues dans la liste d’homologues et les demande s’ils ont le contenu. Le service BITS ne peut télécharger du contenu qu’à partir de serveurs homologues authentifiés. Le client et le serveur s’authentifient initialement mutuellement à l’aide de Kerberos, puis échangent des certificats auto-signés pour l’authentification lors du téléchargement et de la découverte de contenu.

Le service BITS télécharge le contenu à partir du premier homologue authentifié pour répondre à la demande. Si un homologue ne contient pas tout le contenu, le service BITS télécharge ce qu’il peut faire à partir d’un ou plusieurs des homologues avant de télécharger le reste à partir du serveur d’origine. Si aucun des pairs n’a le contenu ou si une erreur se produit lors du téléchargement à partir d’un homologue, BITS télécharge le contenu à partir du serveur d’origine.

Le contenu téléchargé devient disponible pour être utilisé à d’autres homologues uniquement une fois que l’application a validé le contenu des fichiers. Si l’application ne valide pas explicitement le fichier, le fichier est implicitement validé lorsque l’application termine la tâche.

Par défaut, un serveur homologue ne peut fournir du contenu qu’à trois clients simultanément. Si le serveur est actuellement occupé à traiter trois clients, il y aura un délai de réponse aux autres demandes. BITS limite la bande passante utilisée pour traiter le contenu à 1 Mbits/s. Vous pouvez utiliser la stratégie de groupe [MaxBandwidthServed](group-policies.md) pour modifier la limite.

> [!Note]  
> Cette fonctionnalité est prise en charge uniquement dans les réseaux de domaine. la mise en cache d’homologue n’est pas prise en charge sur les groupes de travail ou les réseaux personnels.

Voir aussi [administration du cache d’homologue](/windows/desktop/Bits/administering-the-peer-cache)
 

 

 