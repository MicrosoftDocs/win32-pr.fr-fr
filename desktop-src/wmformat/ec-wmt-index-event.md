---
title: EC_WMT_INDEX_EVENT (kit de développement logiciel (SDK) Windows Media format 11)
description: événement d’index de l’WMT de la EC \_ \_ \_
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- Kit de développement logiciel (SDK) Windows Media format, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- ASF (Advanced Systems Format), EC_WMT_INDEX_EVENT
- ASF (format avancé des systèmes), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032187"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a>EC_WMT_INDEX_EVENT (kit de développement logiciel (SDK) Windows Media format 11)

Envoyé par le kit de développement logiciel (SDK) de format Windows Media lorsqu’une application utilise le writer ASF pour indexer les fichiers Windows Media Video.

Paramètres

*lParam1*

Il peut s’agir de l’un des messages d' **\_ État WMT** suivants.



| Message              | Description                                     |
|----------------------|-------------------------------------------------|
| WMT \_ démarré         | L’indexation a commencé. *lParam2* est égal à zéro.          |
| WMT \_ fermé          | L’indexation est terminée. *lParam2* est égal à zéro. |
| progression de l' \_ index WMT \_ | L’indexation est en cours.                        |



 

*lParam2*

Si *lParam1* a été \_ fermé par WMT ou si WMT \_ a démarré, *lParam2* est égal à zéro. Si *lParam1* est \_ \_ la progression de l’index WMT, *lParam2* est une **valeur DWORD** qui exprime la progression en pourcentage de la taille totale du téléchargement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations de référence sur DirectShow QASF**](directshow-qasf-reference.md)
</dt> </dl>

 

 




