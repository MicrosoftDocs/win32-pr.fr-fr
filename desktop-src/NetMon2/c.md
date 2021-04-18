---
description: Glossaire des termes de Moniteur réseau qui commencent par la lettre C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Moniteur réseau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519685"
---
# <a name="c-network-monitor"></a>C (Moniteur réseau)

<dl> <dt>

<span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**attire**
</dt> <dd>

Données de trafic réseau collectées dans des frames. Un fournisseur de paquets réseau (NPP) effectue une capture. Voir aussi [*capture différée*](d.md)et *capture en temps réel*

</dd> <dt>

<span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**fichier de capture**
</dt> <dd>

Fichier créé par Moniteur réseau pour stocker les données capturées. L’extension de nom de fichier. Cap identifie un fichier de capture. Moniteur réseau génère un nom de fichier de capture de manière aléatoire, mais vous pouvez modifier le nom du fichier lorsque vous enregistrez le fichier de capture.

Moniteur réseau crée un fichier de capture chaque fois que le processus de capture démarre, puis laisse le fichier ouvert pendant le processus de capture. Vous ne pouvez pas accéder au contenu d’un fichier de capture tant que le processus de capture n’est pas arrêté et que le fichier de capture n’est pas fermé.

</dd> <dt>

<span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**filtre de capture**
</dt> <dd>

Ensemble de fonctions de Moniteur réseau utilisées pour restreindre les trames entrantes utilisées par une application de fournisseur de paquets réseau (NPP).

</dd> <dt>

<span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**déclencheur de capture**
</dt> <dd>

Événement de déclencheur qui est défini pour arrêter le processus de capture. L’événement de déclencheur de capture peut être un fichier de capture temporaire qui est dirigé vers un niveau spécifique ou un modèle de données qui se produit dans un frame capturé.

</dd> <dt>

<span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**données capturées**
</dt> <dd>

Frames ayant un ensemble défini de critères. Les trames de données sont contenues dans un fichier de capture temporaire.

</dd> <dt>

<span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**statistiques de conversation**
</dt> <dd>

Statistiques du trafic réseau enregistrées pendant une capture. Ces statistiques incluent les informations de station et de session qui commencent au démarrage du processus de capture et se terminent à l’arrêt de la capture. Si vous suspendez le processus de capture, Moniteur réseau continue à ajouter des statistiques lorsque vous reprenez le processus. Pour récupérer des statistiques de conversation, appelez la méthode **GetConversationStatistics** pour l’interface que vous utilisez.

</dd> </dl>

 

 



