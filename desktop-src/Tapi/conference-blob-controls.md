---
description: Le diagramme suivant illustre les principaux objets impliqués dans les contrôles blob de conférence TAPI 3. Les interfaces affichées sont des liens hypertexte vers les pages de référence appropriées.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Contrôles blob de conférence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527225"
---
# <a name="conference-blob-controls"></a>Contrôles blob de conférence

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Le diagramme suivant illustre les principaux objets impliqués dans les contrôles blob de conférence TAPI 3. Les interfaces affichées sont des liens hypertexte vers les pages de référence appropriées.

![interfaces et contrôles d’objet blob de conférence](images/rendblob.png)

L’objet blob de conférence contient des informations spécifiques au fournisseur sur un objet de conférence. Un pointeur vers l’objet blob d’interface [**ITConferenceBlob**](itconferenceblob.md) est obtenu en exécutant QueryInterface sur [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference). L’interface **ITConferenceBlob** fournit des méthodes pour la manipulation de base d’un objet blob de conférence générique. Une application utilisant des objets BLOB de conférence non-SDP doit implémenter ses propres méthodes pour la manipulation détaillée.

Rendezvous fournit l’interface [**ITSdp**](itsdp.md) pour manipuler les objets BLOB de conférence SDP. Le SDP est un protocole permettant de décrire les sessions multimédias et leurs informations de planification associées. Pour plus d’informations sur le protocole SDP, localisez la norme IETF (Internet Engineering Task Force) RFC 2327 intitulée « SDP : session Description Protocol ». Si l’interface **ITSDP** existe pour un objet blob de conférence donné, vous pouvez obtenir un pointeur vers celle-ci en exécutant **QueryInterface** sur [**ITConferenceBlob**](itconferenceblob.md).

Pour les objets BLOB de conférence SDP, les interfaces [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md)et [**ITMedia**](itmedia.md) permettent un contrôle détaillé du temps de conférence SDP et des caractéristiques du support.

 

 



