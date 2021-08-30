---
description: Événement par utilisateur généré par une tentative de lecture de contenu avec une application multimédia connectée aux contrôles parentaux.
ms.assetid: 478cc11e-afbd-411a-ab84-b8ca7c3aa503
title: Événement WPCEVENT_MEDIA_PLAYBACK (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036f88b657ea53a0d1a44679cc55c5cd109f9d16cada16f1812d301b472ef93b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951133"
---
# <a name="wpcevent_media_playback-event"></a>Événement de lecture du \_ média WPCEVENT \_

Événement par utilisateur généré par une tentative de lecture de contenu avec une application multimédia connectée aux contrôles parentaux.


```C++
const EVENT_DESCRIPTOR WPCEVENT_MEDIA_PLAYBACK = {0x6, 0x0, 0x10, 0x4, 0x16, 0x6, 0x8000000000000030};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AppName* 
</dt> <dd>

Nom de l’application multimédia qui génère l’événement.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Version de l’application multimédia qui génère l’événement.

</dd> <dt>

*MediaType* 
</dt> <dd>

Valeur de l’énumération de [**\_ \_ type de média WPC**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_type) qui indique des informations sur le type de fichier multimédia auquel vous accédez.

</dd> <dt>

*Chemin d’accès* 
</dt> <dd>

Chemin d’accès à la source du contenu multimédia.

</dd> <dt>

*Titre* 
</dt> <dd>

Métadonnées de titre pour le contenu.

</dd> <dt>

*PML* 
</dt> <dd>

Niveau de gestion parental.

</dd> <dt>

*Album* 
</dt> <dd>

Métadonnées de l’album pour le contenu.

</dd> <dt>

*Explicite* 
</dt> <dd>

Valeur de l’énumération [**WPC \_ Media \_ Explicit**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_explicit) qui indique des informations sur l’évaluation explicite du fichier multimédia.

</dd> <dt>

*Motif* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des API de journalisation pour les contrôles parentaux](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




