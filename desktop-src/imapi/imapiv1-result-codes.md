---
title: Codes de résultat IMAPIv1 (Imapierror. h)
description: Les méthodes des interfaces IMAPi retournent S \_ OK si la méthode a réussi. Dans le cas contraire, elles retournent l’un des codes de résultat suivants.
ms.assetid: 0143ad10-9b65-4621-9bed-71dadd38c3fc
topic_type:
- apiref
api_name:
- IMAPI_S_PROPERTIESIGNORED
- IMAPI_S_BUFFER_TO_SMALL
- IMAPI_E_NOTOPENED
- IMAPI_E_NOTINITIALIZED
- IMAPI_E_USERABORT
- IMAPI_E_GENERIC
- IMAPI_E_MEDIUM_NOTPRESENT
- IMAPI_E_MEDIUM_INVALIDTYPE
- IMAPI_E_DEVICE_NOPROPERTIES
- IMAPI_E_DEVICE_NOTACCESSIBLE
- IMAPI_E_DEVICE_NOTPRESENT
- IMAPI_E_DEVICE_INVALIDTYPE
- IMAPI_E_INITIALIZE_WRITE
- IMAPI_E_INITIALIZE_ENDWRITE
- IMAPI_E_FILESYSTEM
- IMAPI_E_FILEACCESS
- IMAPI_E_DISCINFO
- IMAPI_E_TRACKNOTOPEN
- IMAPI_E_TRACKOPEN
- IMAPI_E_DISCFULL
- IMAPI_E_BADJOLIETNAME
- IMAPI_E_INVALIDIMAGE
- IMAPI_E_NOACTIVEFORMAT
- IMAPI_E_NOACTIVERECORDER
- IMAPI_E_WRONGFORMAT
- IMAPI_E_ALREADYOPEN
- IMAPI_E_WRONGDISC
- IMAPI_E_FILEEXISTS
- IMAPI_E_STASHINUSE
- IMAPI_E_DEVICE_STILL_IN_USE
- IMAPI_E_LOSS_OF_STREAMING
- IMAPI_E_COMPRESSEDSTASH
- IMAPI_E_ENCRYPTEDSTASH
- IMAPI_E_NOTENOUGHDISKFORSTASH
- IMAPI_E_REMOVABLESTASH
- IMAPI_E_CANNOT_WRITE_TO_MEDIA
- IMAPI_E_TRACK_NOT_BIG_ENOUGH
api_location:
- Imapierror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80e8aba2a2d3d12628a45c6716c6f94a405d752f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739981"
---
# <a name="imapiv1-result-codes"></a>Codes de résultat IMAPIv1

Les méthodes des interfaces IMAPi retournent S \_ OK si la méthode a réussi. Dans le cas contraire, elles retournent l’un des codes de résultat suivants.



| Constante/valeur                                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMAPI_S_PROPERTIESIGNORED"></span><span id="imapi_s_propertiesignored"></span><dl> <dt>**\_ IMAPI \_PROPERTIESIGNORED**</dt> <dt>0x40200</dt> </dl>                   | Une propriété inconnue a été passée dans un jeu de propriétés et elle a été ignorée.<br/>                                                                                                                                                                              |
| <span id="IMAPI_S_BUFFER_TO_SMALL"></span><span id="imapi_s_buffer_to_small"></span><dl> <dt>**\_ IMAPI \_Mémoire tampon S \_ vers \_ petite**</dt> <dt>0x40201</dt> </dl>                       | La mémoire tampon de sortie est trop petite.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTOPENED"></span><span id="imapi_e_notopened"></span><dl> <dt>**\_ IMAPI \_NOTOPENED**</dt> <dt>0x8004020b</dt> </dl>                                        | Un appel à [**IDiscMaster :: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) n’a pas été effectué.<br/>                                                                                                                                                                        |
| <span id="IMAPI_E_NOTINITIALIZED"></span><span id="imapi_e_notinitialized"></span><dl> <dt>**\_ IMAPI \_NOTINITIALIZED**</dt> <dt>0x8004020c</dt> </dl>                         | Un objet enregistreur n’a pas été initialisé.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_USERABORT"></span><span id="imapi_e_userabort"></span><dl> <dt>**\_ IMAPI \_USERABORT**</dt> <dt>0x8004020d</dt> </dl>                                        | L’utilisateur a annulé l’opération.<br/>                                                                                                                                                                                                                  |
| <span id="IMAPI_E_GENERIC"></span><span id="imapi_e_generic"></span><dl> <dt>**\_ IMAPI 0x8004020e \_ générique**</dt> <dt></dt> </dl>                                              | Une erreur générique s’est produite.<br/>                                                                                                                                                                                                                         |
| <span id="IMAPI_E_MEDIUM_NOTPRESENT"></span><span id="imapi_e_medium_notpresent"></span><dl> <dt>**\_ IMAPI E \_ \_ indique absent**</dt> <dt>0x8004020f</dt> </dl>               | Il n’y a pas de disque dans l’appareil.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_MEDIUM_INVALIDTYPE"></span><span id="imapi_e_medium_invalidtype"></span><dl> <dt>**\_ IMAPI E \_ \_ INVALIDTYPE**</dt> <dt>0x80040210</dt> </dl>            | Le support n’est pas un type qui peut être utilisé.<br/>                                                                                                                                                                                                         |
| <span id="IMAPI_E_DEVICE_NOPROPERTIES"></span><span id="imapi_e_device_noproperties"></span><dl> <dt>**\_ IMAPI 0x80040211 \_ de \_ Propriétés de l’appareil E**</dt> <dt></dt> </dl>         | L’enregistreur ne prend pas en charge les propriétés.<br/>                                                                                                                                                                                                     |
| <span id="IMAPI_E_DEVICE_NOTACCESSIBLE"></span><span id="imapi_e_device_notaccessible"></span><dl> <dt>**\_ IMAPI \_ \_ NOTACCESSIBLE**</dt> de l’appareil <dt>0x80040212</dt> </dl>      | L’appareil ne peut pas être utilisé ou est déjà en cours d’utilisation.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DEVICE_NOTPRESENT"></span><span id="imapi_e_device_notpresent"></span><dl> <dt>**\_ IMAPI \_ \_ Indique absent**</dt> de l’appareil <dt>0x80040213</dt> </dl>               | L’appareil n’est pas présent ou a été supprimé.<br/>                                                                                                                                                                                                    |
| <span id="IMAPI_E_DEVICE_INVALIDTYPE"></span><span id="imapi_e_device_invalidtype"></span><dl> <dt>**\_ IMAPI \_ \_ INVALIDTYPE**</dt> de l’appareil <dt>0x80040214</dt> </dl>            | L’enregistreur ne prend pas en charge une opération.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_INITIALIZE_WRITE"></span><span id="imapi_e_initialize_write"></span><dl> <dt>**\_ IMAPI E \_ Initialize \_ Write**</dt> <dt>0x80040215</dt> </dl>                  | L’interface du lecteur n’a pas pu être initialisée pour l’écriture.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_INITIALIZE_ENDWRITE"></span><span id="imapi_e_initialize_endwrite"></span><dl> <dt>**\_ IMAPI E \_ Initialize \_ ENDWRITE**</dt> <dt>0x80040216</dt> </dl>         | L’interface du lecteur n’a pas pu être initialisée pour la fermeture.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_FILESYSTEM"></span><span id="imapi_e_filesystem"></span><dl> <dt>**\_ IMAPI 0x80040217 de \_ système de fichiers**</dt> <dt></dt> </dl>                                     | Une erreur s’est produite lors de l’activation ou de la désactivation de l’accès au système de fichiers ou lors de la détection de l’insertion automatique.<br/>                                                                                                                                                 |
| <span id="IMAPI_E_FILEACCESS"></span><span id="imapi_e_fileaccess"></span><dl> <dt>**\_ IMAPI 0x80040218 E \_ FILEACCESS**</dt> <dt></dt> </dl>                                     | Une erreur s’est produite lors de l’écriture du fichier image.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DISCINFO"></span><span id="imapi_e_discinfo"></span><dl> <dt>**\_ IMAPI \_DISCINFO**</dt> <dt>0x80040219</dt> </dl>                                           | Une erreur s’est produite lors de la tentative de lecture des données du disque à partir de l’appareil.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_TRACKNOTOPEN"></span><span id="imapi_e_tracknotopen"></span><dl> <dt>**\_ IMAPI \_TRACKNOTOPEN**</dt> <dt>0x8004021a</dt> </dl>                               | Une piste audio n’est pas ouverte pour l’écriture.<br/>                                                                                                                                                                                                           |
| <span id="IMAPI_E_TRACKOPEN"></span><span id="imapi_e_trackopen"></span><dl> <dt>**\_ IMAPI \_TRACKOPEN**</dt> <dt>0x8004021b</dt> </dl>                                        | Une piste audio ouverte est déjà en cours de transfert.<br/>                                                                                                                                                                                                      |
| <span id="IMAPI_E_DISCFULL"></span><span id="imapi_e_discfull"></span><dl> <dt>**\_ IMAPI \_DISCFULL**</dt> <dt>0x8004021c</dt> </dl>                                           | Le disque ne peut pas contenir plus de données.<br/>                                                                                                                                                                                                               |
| <span id="IMAPI_E_BADJOLIETNAME"></span><span id="imapi_e_badjolietname"></span><dl> <dt>**\_ IMAPI \_BADJOLIETNAME**</dt> <dt>0x8004021d</dt> </dl>                            | L’application a essayé d’ajouter un élément mal nommé sur un disque.<br/>                                                                                                                                                                                     |
| <span id="IMAPI_E_INVALIDIMAGE"></span><span id="imapi_e_invalidimage"></span><dl> <dt>**\_ IMAPI \_INVALIDIMAGE**</dt> <dt>0x8004021e</dt> </dl>                               | L’image intermédiaire n’est pas adaptée à une gravure. Il a été endommagé ou effacé et n’a pas de contenu utilisable.<br/>                                                                                                                                          |
| <span id="IMAPI_E_NOACTIVEFORMAT"></span><span id="imapi_e_noactiveformat"></span><dl> <dt>**\_ IMAPI \_NOACTIVEFORMAT**</dt> <dt>0x8004021f</dt> </dl>                         | Un maître de format actif n’a pas été sélectionné à l’aide de [**IDiscMaster :: SetActiveDiscMasterFormat**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscmasterformat).<br/>                                                                                                      |
| <span id="IMAPI_E_NOACTIVERECORDER"></span><span id="imapi_e_noactiverecorder"></span><dl> <dt>**\_ IMAPI \_NOACTIVERECORDER**</dt> <dt>0x80040220</dt> </dl>                   | Un enregistreur de disque actif n’a pas été sélectionné à l’aide de [**IDiscMaster :: SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder).<br/>                                                                                                              |
| <span id="IMAPI_E_WRONGFORMAT"></span><span id="imapi_e_wrongformat"></span><dl> <dt>**\_ IMAPI \_WRONGFORMAT**</dt> <dt>0x80040221</dt> </dl>                                  | Un appel à [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) a été effectué lorsque [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) est le format actif, ou vice versa. Pour utiliser un format différent, modifiez le format et effacez le contenu du fichier image.<br/> |
| <span id="IMAPI_E_ALREADYOPEN"></span><span id="imapi_e_alreadyopen"></span><dl> <dt>**\_ IMAPI \_ALREADYOPEN**</dt> <dt>0x80040222</dt> </dl>                                  | Un appel à [**IDiscMaster :: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) a déjà été effectué sur cet objet par votre application.<br/>                                                                                                                            |
| <span id="IMAPI_E_WRONGDISC"></span><span id="imapi_e_wrongdisc"></span><dl> <dt>**\_ IMAPI \_WRONGDISC**</dt> <dt>0x80040223</dt> </dl>                                        | Le disque multi-session IMAPi a été supprimé de l’enregistreur actif.<br/>                                                                                                                                                                           |
| <span id="IMAPI_E_FILEEXISTS"></span><span id="imapi_e_fileexists"></span><dl> <dt>**\_ IMAPI E \_ FILEEXISTS**</dt> <dt>0x80040224</dt> </dl>                                     | Le fichier à ajouter se trouve déjà dans le fichier image et l’indicateur de remplacement n’a pas été défini.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_STASHINUSE"></span><span id="imapi_e_stashinuse"></span><dl> <dt>**\_ IMAPI \_STASHINUSE**</dt> <dt>0x80040225</dt> </dl>                                     | Une autre application utilise déjà le fichier de dissimulation IMAPi requis pour effectuer une copie intermédiaire d’une image de disque. Réessayez plus tard.<br/>                                                                                                                                        |
| <span id="IMAPI_E_DEVICE_STILL_IN_USE"></span><span id="imapi_e_device_still_in_use"></span><dl> <dt>**\_ IMAPI \_Appareil E \_ toujours \_ en cours d' \_ utilisation**</dt> <dt>0x80040226</dt> </dl>       | Une autre application utilise déjà cet appareil, donc IMAPi ne peut pas accéder à l’appareil.<br/>                                                                                                                                                              |
| <span id="IMAPI_E_LOSS_OF_STREAMING"></span><span id="imapi_e_loss_of_streaming"></span><dl> <dt>**\_ IMAPI \_Perte \_ de 0x80040227 de diffusion en \_ continu**</dt> <dt></dt> </dl>              | La diffusion en continu du contenu a été perdue. une mémoire tampon sous-exécution peut s’être produite.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_COMPRESSEDSTASH"></span><span id="imapi_e_compressedstash"></span><dl> <dt>**\_ IMAPI \_COMPRESSEDSTASH**</dt> <dt>0x80040228</dt> </dl>                      | La dissimulation se trouve sur un volume compressé et ne peut pas être lue.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_ENCRYPTEDSTASH"></span><span id="imapi_e_encryptedstash"></span><dl> <dt>**\_ IMAPI \_ENCRYPTEDSTASH**</dt> <dt>0x80040229</dt> </dl>                         | La dissimulation se trouve sur un volume chiffré et ne peut pas être lue.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTENOUGHDISKFORSTASH"></span><span id="imapi_e_notenoughdiskforstash"></span><dl> <dt>**\_ IMAPI \_NOTENOUGHDISKFORSTASH**</dt> <dt>0x8004022a</dt> </dl>    | L’espace libre est insuffisant pour créer le fichier de dissimulation sur le volume spécifié.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_REMOVABLESTASH"></span><span id="imapi_e_removablestash"></span><dl> <dt>**\_ IMAPI \_REMOVABLESTASH**</dt> <dt>0x8004022b</dt> </dl>                         | L’emplacement de dissimulation sélectionné se trouve sur un support amovible.<br/>                                                                                                                                                                                              |
| <span id="IMAPI_E_CANNOT_WRITE_TO_MEDIA"></span><span id="imapi_e_cannot_write_to_media"></span><dl> <dt>**\_ IMAPI E \_ Impossible \_ \_ d’écrire sur le \_ support**</dt> <dt>0x8004022c</dt> </dl> | Impossible d’écrire dans le média.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_TRACK_NOT_BIG_ENOUGH"></span><span id="imapi_e_track_not_big_enough"></span><dl> <dt>**\_ IMAPI \_Le rail E \_ n’est pas \_ \_ assez grand**</dt> <dt>0x8004022d</dt> </dl>    | La piste n’est pas assez grande.<br/>                                                                                                                                                                                                                      |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Imapierror. h</dt> </dl> |



 

 





