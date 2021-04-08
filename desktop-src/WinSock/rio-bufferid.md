---
description: Spécifie un descripteur de mémoire tampon inscrit utilisé avec les extensions d’e/s inscrites Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034263"
---
# <a name="rio_bufferid"></a>\_l’élément BUFFERID Rio

Le **typedef \_ l’élément bufferID** typedef spécifie un descripteur de mémoire tampon inscrit utilisé avec les extensions d’e/s inscrites Winsock.


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

**\_l’élément BUFFERID Rio**
</dt> <dd>

Type de données qui spécifie un descripteur de mémoire tampon inscrit utilisé avec les demandes d’envoi et de réception.

</dd> </dl>

## <a name="remarks"></a>Notes

Les extensions d’e/s inscrites par Winsock fonctionnent principalement sur les mémoires tampons enregistrées à l’aide d’objets **Rio \_ l’élément bufferID** . Une application obtient un **\_ l’élément bufferID Rio** pour une mémoire tampon existante à l’aide de la fonction [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) . Une application peut libérer une inscription à l’aide de la fonction [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) .

Lorsqu’une mémoire tampon existante est inscrite en tant qu’objet **Rio \_ l’élément bufferID** à l’aide de la fonction [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) , certaines ressources internes sont allouées à partir de la mémoire physique et la mémoire tampon de l’application existante est verrouillée dans la mémoire physique. La fonction [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) est appelée pour annuler l’inscription de la mémoire tampon, libérer ces ressources internes et autoriser le déverrouillage et la libération de la mémoire tampon à partir de la mémoire physique.

L’inscription et la désinscription répétées des tampons d’application à l’aide des extensions d’e/s inscrites par Winsock peuvent entraîner une dégradation significative des performances. Les approches de gestion des mémoires tampons suivantes doivent être prises en compte lors de la conception d’une application à l’aide des extensions d’e/s inscrites par Winsock pour réduire l’inscription et la désinscription répétées des mémoires tampons d’application :

-   • Optimisez la réutilisation des tampons.
-   • Conserver un pool limité de mémoires tampons enregistrées inutilisées pour une utilisation par l’application.
-   • Gérer un pool limité de mémoires tampons enregistrées et effectuer des copies de tampon entre ces mémoires tampons enregistrées et d’autres tampons non inscrits.

Le **typedef \_ l’élément bufferID** typedef est défini dans le fichier d’en-tête *Mswsockdef. h* qui est automatiquement inclus dans le fichier d’en-tête *mswsock. h* . Le fichier d’en-tête *Mswsockdef. h* ne doit jamais être utilisé directement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Mswsockdef. h (inclure mswsock. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RIO \_ buf**](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))
</dt> <dt>

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> </dl>

 

 
