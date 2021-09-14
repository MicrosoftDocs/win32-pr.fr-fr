---
title: EC_WMT_EVENT (kit de développement logiciel (SDK) Windows Media Format 11)
description: '\_événement EC WMT \_'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- Windows Media Format SDK, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- gestion des droits numériques (DRM), EC_WMT_EVENT
- DRM (Digital Rights Management), EC_WMT_EVENT
- ASF (Advanced Systems Format), EC_WMT_EVENT
- ASF (format avancé des systèmes), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295186"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a>EC_WMT_EVENT (kit de développement logiciel (SDK) Windows Media Format 11)

envoyé par le kit de développement logiciel (SDK) de Format multimédia Windows lorsqu’une application utilise le filtre de lecteur asf pour lire des fichiers asf protégés par la gestion des droits numériques (DRM).

Paramètres

*lParam1*

Il peut s’agir de l’une des valeurs d’État WMT suivantes \_ .



| \_Message d’État WMT           | Description                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| WMT \_ aucun \_ droit               | Le fichier est protégé par la version 1 de DRM et l’application n’a aucun droit pour effectuer l’action demandée.                    |
| \_licence d’acquisition WMT \_         | Le processus d’acquisition de licence est terminé. (Cela ne signifie pas nécessairement qu’une licence a été acquise avec succès.) |
| WMT \_ aucun \_ droit \_ ex           | Le fichier est protégé par la version 7 de DRM et l’application ne dispose pas des droits nécessaires pour exécuter l’action demandée.                    |
| WMT \_ a besoin d’une \_ individualisation | La licence autorise uniquement les applications individuelles à exécuter l’action demandée.                                           |
| \_personnalisable WMT            | Le processus d’individualisation est en cours d’exécution ou terminé.                                                    |



 

*lParam2*

pointeur vers une structure de **données d’événement « AM \_ \_ \_ WMT** » qui contient des informations sur l’événement dans le pointeur de membre **pData** , ainsi qu’un code d’état **HRESULT** envoyé par le kit de développement logiciel (SDK) de Format multimédia Windows. La valeur de *lParam2* dépend de la valeur de *lParam1*, comme décrit dans le tableau suivant. (les structures « WM \_ » sont définies dans le kit de développement logiciel (SDK) Format multimédia Windows.)



| Si lParam1 est...              | \_Données d' \_ événement WMT am \_ . pdata est...                            |
|-------------------------------|-------------------------------------------------------------|
| WMT \_ aucun \_ droit               | Pointeur vers une chaîne **WCHAR** contenant une URL de Challenge. |
| \_licence d’acquisition WMT \_         | Pointeur vers une structure **de \_ \_ \_ données de licence WM** .        |
| WMT \_ aucun \_ droit \_ ex           | Pointeur vers une structure **de \_ \_ \_ données de licence WM** .        |
| WMT \_ a besoin d’une \_ individualisation | NULL.                                                       |
| \_personnalisable WMT            | Pointeur vers une structure d’état de l' **\_ \_ individualisation WM** .     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de Rights Management numérique**](digital-rights-management-features.md)
</dt> <dt>

[**DirectShow Référence QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




