---
description: le Service de réplication de fichiers (FRS) est déconseillé dans Windows Server 2008 R2
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: le Service de réplication de fichiers (FRS) est déconseillé dans Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72940d2b73b807d5420aface3096714ac132df2095d154fc7563717c33fa6e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759939"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a>le Service de réplication de fichiers (FRS) est déconseillé dans Windows Server 2008 R2

## <a name="platform"></a>Plateforme

 **serveurs-** Windows Server 2008 R2  

## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité-** Rapide  
**Fréquence-** Rapide  


## <a name="description"></a>Description

dans Windows Server 2008 R2, le Service de réplication de fichiers (FRS) ne peut pas être utilisé pour répliquer des dossiers système de fichiers DFS (DFS) ou des données personnalisées (autres que SYSVOL). un contrôleur de domaine Windows Server 2008 R2 peut toujours utiliser frs pour répliquer le contenu du partage sysvol dans un domaine qui utilise le service frs pour répliquer le partage sysvol entre les contrôleurs de domaine. toutefois, les serveurs Windows Server 2008 R2 ne peuvent pas utiliser le service FRS pour répliquer le contenu d’un jeu de réplicas séparé du partage SYSVOL. Le service réplication DFS remplace le service FRS et peut être utilisé pour répliquer le contenu du partage SYSVOL, les dossiers DFS, ainsi que d’autres données personnalisées (autres que SYSVOL). Migrez tous les jeux de réplicas FRS non SYSVOL vers réplication DFS. Nous vous recommandons également de migrer la réplication du partage SYSVOL de FRS vers réplication DFS, car réplication DFS est plus robuste, évolutive et offre de meilleures performances de réplication que FRS.

## <a name="manifestation"></a>Manifestation

La réplication FRS de données personnalisées est irréversible sur la mise à niveau sur place. La seule façon de procéder à une récupération à partir de cette situation consiste à réinstaller un système d’exploitation plus ancien sur le serveur et à réinitialiser la réplication FRS. les serveurs qui ont été mis à niveau vers Windows Server 2008 R2 ne sont pas autorisés à participer à des groupes de réplication FRS existants.

## <a name="mitigation-of-impact"></a>Atténuation de l’impact

Pour éviter les problèmes qui peuvent se produire suite à ces modifications, migrez les jeux de réplication FRS personnalisés vers réplication DFS. Le service réplication DFS présente de nombreux avantages par rapport à FRS, y compris des outils de gestion améliorés, des performances supérieures et une gestion déléguée.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Vue d’ensemble de FRS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))
-   [Réplication du système de fichiers DFS : Forum Aux Questions](/windows-server/storage/dfs-replication/dfsr-faq)
-   [Guide de migration de la réplication SYSVOL : Réplication FRS vers DFS](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
