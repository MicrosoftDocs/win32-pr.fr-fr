---
description: Événement par utilisateur généré par une tentative de lecture de contenu avec une application multimédia connectée aux contrôles parentaux.
ms.assetid: 478cc11e-afbd-411a-ab84-b8ca7c3aa503
title: Événement WPCEVENT_MEDIA_PLAYBACK (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdf4e884cc0e87f579d245676f78232a5ae0177
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522507"
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

*Explicitement* 
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des API de journalisation pour les contrôles parentaux](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




