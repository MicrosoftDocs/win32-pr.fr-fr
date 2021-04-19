---
description: Événement par utilisateur généré lors de la tentative de téléchargement de fichiers à partir du Web. Cet événement est généré par les applications demandées par les contrôles parentaux.
ms.assetid: 2291fc75-55e5-417e-b393-748750a5b3d6
title: Événement WPCEVENT_WEB_FILEDOWNLOAD (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66bb04a53589a1cae41e2ba7d7a9c00835452e87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538718"
---
# <a name="wpcevent_web_filedownload-event"></a>\_ \_ Événement FILEDOWNLOAD Web WPCEVENT

Événement par utilisateur généré lors de la tentative de téléchargement de fichiers à partir du Web. Cet événement est généré par les applications demandées par les contrôles parentaux.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_FILEDOWNLOAD = {0xa, 0x0, 0x10, 0x4, 0x18, 0xa, 0x8000000000000030};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*URL* 
</dt> <dd>

Source de l’URL qui tente de télécharger.

</dd> <dt>

*AppName* 
</dt> <dd>

Nom de l’application qui génère l’événement.

</dd> <dt>

*Version* 
</dt> <dd>

Version de l’application qui génère l’événement.

</dd> <dt>

*Bloqué* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

</dd> <dt>

*Chemin d’accès* 
</dt> <dd>

Chemin d’accès de destination du fichier.

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

 

 




