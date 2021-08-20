---
description: Windows met en cache les données de fichiers qui sont lues à partir des disques et écrites sur les disques.
ms.assetid: 0865c741-63e3-4246-ba69-801b02153e4a
title: Mise en cache des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82295edb7126c73e1a3801e7140fc9a62763b1e3400ef3b568571251b2f6cc40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117997321"
---
# <a name="file-caching"></a>Mise en cache des fichiers

Par défaut, Windows met en cache les données de fichier lues à partir de disques et écrites sur des disques. Cela implique que les opérations de lecture lisent les données du fichier à partir d’une zone de la mémoire système appelée « cache des fichiers système », plutôt qu’à partir du disque physique. En conséquence, les opérations d’écriture écrivent les données de fichier dans le cache de fichiers système plutôt que sur le disque, et ce type de cache est appelé cache de réinscription. La mise en cache est gérée par objet de fichier.

la mise en cache se produit dans le sens du *gestionnaire de cache*, qui fonctionne en continu pendant que Windows est en cours d’exécution. Les données de fichier dans le cache de fichiers système sont écrites sur le disque à des intervalles déterminés par le système d’exploitation, et la mémoire utilisée précédemment par ces données de fichier est libérée. cela s’appelle le *vidage* du cache. La stratégie de retardement de l’écriture des données dans le fichier et de leur conservation dans le cache jusqu’à ce que le cache soit vidé est appelée écriture différée, et elle est déclenchée par le gestionnaire de caches à un intervalle de temps d’arrêt. Le moment auquel un bloc de données de fichier est vidé dépend en partie de la durée pendant laquelle il a été stocké dans le cache et de la période écoulée depuis le dernier accès aux données lors d’une opération de lecture. Cela garantit que les données de fichier fréquemment lues resteront accessibles dans le cache de fichiers système pendant le temps maximal imparti.

Ce processus de mise en cache des données de fichier est illustré dans la figure suivante.

![processus de mise en cache des données de fichier](images/fig3.png)

Comme illustré par les flèches pleines de la figure précédente, une zone de données de 256 Ko est lue dans un « emplacement » du cache de 256 Ko dans l’espace d’adressage du système lorsqu’elle est demandée pour la première fois par le gestionnaire de cache lors d’une opération de lecture de fichier. Un processus en mode utilisateur copie ensuite les données de cet emplacement dans son propre espace d’adressage. Lorsque le processus a terminé son accès aux données, il enregistre les données modifiées dans le même emplacement dans la mémoire cache du système, comme indiqué par la flèche en pointillé entre l’espace d’adressage du processus et la mémoire cache du système. Lorsque le gestionnaire de cache a déterminé que les données ne seront plus nécessaires pendant un certain temps, il réenregistre les données modifiées dans le fichier sur le disque, comme indiqué par la flèche en pointillés entre le cache système et le disque.

La quantité d’amélioration des performances d’e/s offerte par la mise en cache des données de fichiers dépend de la taille du bloc de données de fichier en cours de lecture ou d’écriture. Lorsque des blocs volumineux de données de fichier sont lus et écrits, il est plus probable que les lectures et écritures sur le disque seront nécessaires pour terminer l’opération d’e/s. Les performances d’e/s seront de plus en plus altérées, car de plus en plus ce type d’opération d’e/s se produit.

Dans ce cas, la mise en cache peut être désactivée. Cette opération s’effectue au moment où le fichier est ouvert en passant l' **indicateur de fichier \_ \_ sans \_ mise en mémoire tampon** comme valeur pour le paramètre *dwFlagsAndAttributes* de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Lorsque la mise en cache est désactivée, toutes les opérations de lecture et d’écriture accèdent directement au disque physique. Toutefois, les métadonnées du fichier peuvent toujours être mises en cache. Pour vider les métadonnées sur le disque, utilisez la fonction [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .

La fréquence à laquelle le vidage se produit est un facteur important qui équilibre les performances du système avec la fiabilité du système. Si le système vide le cache trop souvent, le vidage des opérations d’écriture importantes entraîne une dégradation significative des performances du système. Si le système n’est pas suffisamment vidé, la probabilité est plus élevée que la mémoire système soit épuisée par le cache ou une défaillance soudaine du système (telle qu’une perte d’alimentation de l’ordinateur) se produira avant le vidage. Dans ce dernier cas, les données mises en cache seront perdues.

Pour s’assurer que la quantité de vidage appropriée est levée, le gestionnaire de cache génère un processus chaque seconde appelé Writer différé. Le processus d’écriture différée met en file d’attente une huitième des pages qui n’ont pas été vidées récemment pour être écrites sur le disque. Elle réévalue constamment la quantité de données vidées pour des performances optimales du système et, si davantage de données doivent être écrites, elle met en file d’attente plus de données. Les enregistreurs paresseux ne vident pas les fichiers temporaires, car ils seront supprimés par l’application ou le système.

Certaines applications, telles que les logiciels antivirus, requièrent que leurs opérations d’écriture soient immédiatement vidées sur le disque ; Windows offre cette possibilité via la mise en cache en écriture. Un processus permet la mise en cache en écriture automatique pour une opération d’e/s spécifique en passant l’indicateur d’écriture d’indicateur de fichier dans son appel à [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). **\_ \_ \_** Lorsque la mise en cache en écriture différée est activée, les données sont toujours écrites dans le cache, mais le gestionnaire de cache écrit les données immédiatement sur le disque plutôt que d’effectuer un délai à l’aide de l’outil d’écriture différée. Un processus peut également forcer un vidage d’un fichier qu’il a ouvert en appelant la fonction [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .

Les métadonnées du système de fichiers sont toujours mises en cache. Par conséquent, pour stocker les modifications apportées aux métadonnées sur le disque, le fichier doit être vidé ou ouvert avec l' **indicateur de fichier \_ \_ Write \_ via**.

 

 



