---
description: Envoyé par le filtre de lecteur ASF WM lorsqu’il lit des fichiers ASF protégés par la gestion des droits numériques (DRM).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540356"
---
# <a name="ec_wmt_event-dshowh"></a>EC_WMT_EVENT (DShow. h)

Envoyé par le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) lorsqu’il lit des fichiers ASF protégés par la gestion des droits numériques (DRM).

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Une des valeurs d' **\_ État WMT** suivantes :



| Valeur                         | Description                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| \_licence d’acquisition WMT \_         | Envoyé lorsque le composant DRM a terminé le processus d’acquisition de licence, soit avec succès, soit sans succès. |
| \_personnalisable WMT            | Le processus de mise à niveau de sécurité est terminé, soit avec succès, soit sans succès.                                |
| WMT \_ a besoin d’une \_ individualisation | Le fichier requiert qu’une application reçoive une mise à niveau de sécurité avant d’effectuer l’action demandée.          |
| WMT \_ aucun \_ droit               | L’application ne dispose pas des droits nécessaires pour exécuter l’action demandée sur un fichier protégé par DRM version 1.                |
| WMT \_ aucun \_ droit \_ ex           | L’application ne dispose pas des droits nécessaires pour exécuter l’action demandée sur un fichier protégé par DRM version 7.                |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Pointeur vers une structure de [**\_ données d' \_ événement \_ « am WMT**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) » qui contient des informations sur l’événement ou la **valeur null**. Le membre **pData** de cette structure pointe vers des données supplémentaires, dont le type dépend de la valeur de **lParam1**, comme indiqué dans le tableau suivant.



| lParam1                       | \_Données d' \_ événement WMT am \_ . pdata                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| \_licence d’acquisition WMT \_         | Pointeur vers une structure de [**\_ \_ \_ données de licence WM**](/windows/desktop/wmformat/wm-get-license-data) . Cette structure est documentée dans le kit de développement logiciel (SDK) du format Windows Media. |
| \_personnalisable WMT            | Pointeur désignant une structure d’état de l' [**\_ \_ individualisation WM**](/windows/desktop/wmformat/wm-individualize-status) .                                                        |
| WMT \_ a besoin d’une \_ individualisation | **Valeur null**.                                                                                                                                        |
| WMT \_ aucun \_ droit               | Pointeur vers une chaîne de caractères larges contenant une URL de Challenge.                                                                                   |
| WMT \_ aucun \_ droit \_ ex           | Pointeur vers une structure de [**\_ \_ \_ données de licence WM**](/windows/desktop/wmformat/wm-get-license-data) .                                                               |



 

La valeur de *lParam2* peut être **null**. Vérifiez la valeur avant de déréférencer le pointeur.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour plus d’informations sur l’activation de la lecture de fichiers protégés par DRM, consultez la documentation du kit de développement logiciel (SDK) Windows Media format.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

