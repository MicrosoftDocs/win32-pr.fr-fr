---
description: Présentation de l'architecture
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Présentation de l'architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868270"
---
# <a name="architecture-overview"></a>Présentation de l'architecture

L’architecture WPD peut être divisée en trois processus. Ces processus sont les trois composants principaux d’WPD : l’API, le sérialiseur et le pilote. L’illustration suivante représente les processus et les composants qui constituent l’architecture WPD.

![illustration illustrant les composants API, sérialiseur et pilote d’wpd](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a>Interface de programmation d’applications WPD

L’API WPD est implémentée en tant que serveur COM in-proc. L’API utilise des API Microsoft Win32 standard pour communiquer avec le pilote WPD approprié. Un composant appelé sérialiseur WPD est utilisé par les objets d’API et le pilote pour regrouper ou décompresser des paramètres vers ou depuis Windows Driver Foundation (WDF)-mémoires tampons de l’infrastructure de pilote de mode utilisateur (UMDF).

## <a name="the-wpd-serializer"></a>Sérialiseur WPD

Le sérialiseur WPD est implémenté en tant que serveur COM in-proc. L’API WPD utilise le sérialiseur pour compresser les commandes et les paramètres dans les tampons de messages envoyés au pilote. Le pilote utilise le sérialiseur pour décompresser les tampons de messages en vue de leur traitement. Le pilote utilise également le sérialiseur pour compresser les données et les paramètres dans les tampons de réponse qui sont retournés à l’API WPD, et l’API WPD utilise le sérialiseur pour décompresser ces tampons de réponse pour revenir aux appelants.

## <a name="wpd-driver"></a>Pilote WPD

Le pilote WPD est implémenté en tant que pilote WDF (Windows Driver Foundation) standard (UMDF). Les pilotes WPD sont hébergés par UMDF dans un processus distinct appelé hôte de pilote.

Le pilote reçoit des messages du réflecteur UMDF (cela n’est pas indiqué dans le diagramme, car la manière dont les tampons sont reçus n’a pas d’importance pour le pilote. Pour plus d’informations, consultez la documentation UMDF. Le pilote implémente un gestionnaire de code de contrôle d’e/s (IOCL) spécifique à WPD pour traiter les messages WPD reçus par l’API WPD. Le pilote utilise le sérialiseur WPD pour décompresser des commandes et des paramètres à partir de ces mémoires tampons de messages, et pour empaqueter la réponse dans la mémoire tampon de retour.

Les pilotes WPD peuvent communiquer avec leurs appareils en passant par un pilote en mode noyau, généralement accessible via les opérations de fichier Win32 (c’est-à-dire, CreateFile, ReadFile, WriteFile, etc.). Pour les bus courants, Microsoft fournira des pilotes de noyau standard que les fournisseurs pourront utiliser, ce qui permettra aux fournisseurs d’envoyer une solution de pilote en mode utilisateur uniquement. En outre, pour les appareils MTP (Media Transfer Protocol) et MSC (Storage-Class), Microsoft fournira des pilotes de classe WPD.

Pour plus d’informations sur les pilotes WPD, consultez la documentation du pilote des appareils mobiles Windows dans le kit de pilotes Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble de l’application**](application-overview.md)
</dt> </dl>

 

 



