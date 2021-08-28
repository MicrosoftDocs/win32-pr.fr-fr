---
description: Définit le comportement du programme de résolution source. Ces indicateurs sont également utilisés par les gestionnaires de modèles et les gestionnaires de flux d’octets.
ms.assetid: fe0b9090-5d2a-41a4-a806-57c874d3b3a2
title: Indicateurs de résolveur source (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c779a54467390abf6cfb186f6b76043fd19617f5d129b88e6697a45c01708510
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847819"
---
# <a name="source-resolver-flags"></a>Indicateurs de résolveur source

Définit le comportement du programme de résolution source. Ces indicateurs sont également utilisés par les gestionnaires de modèles et les gestionnaires de flux d’octets.



| Constante/valeur                                                                                                                                                                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_RESOLUTION_MEDIASOURCE"></span><span id="mf_resolution_mediasource"></span><dl> <dt>**MF \_ Resolution \_ MEDIASOURCE**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                           | Tentative de création d’une source de média.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="MF_RESOLUTION_BYTESTREAM"></span><span id="mf_resolution_bytestream"></span><dl> <dt>**MF \_ RÉSOLUTION \_ BYTESTREAM**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                              | Tentative de création d’un flux d’octets.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="MF_RESOLUTION_CONTENT_DOES_NOT_HAVE_TO_MATCH_EXTENSION_OR_MIME_TYPE_"></span><span id="mf_resolution_content_does_not_have_to_match_extension_or_mime_type_"></span><dl> Le <dt> **\_ \_ contenu de résolution MF \_ ne \_ \_ doit pas nécessairement \_ correspondre à l' \_ \_ extension ou au \_ \_ \_ type MIME**</dt> <dt>0x00000010</dt> </dl> | Si la résolution de la source échoue à l’aide du gestionnaire de flux d’octets qui est inscrit pour l’extension de nom de fichier ou de type MIME, le programme de résolution source énumère tous les gestionnaires de flux d’octets inscrits.<br/> Les gestionnaires de flux d’octets sont inscrits par extension de nom de fichier ou type MIME. Initialement, le programme de résolution source tente d’utiliser un gestionnaire qui correspond à l’extension de nom de fichier ou au type MIME. En cas d’échec, par défaut, la résolution de source entière échoue et le programme de résolution source renvoie un code d’erreur à l’application. Toutefois, si cet indicateur est spécifié, le programme de résolution source continue à énumérer tous les gestionnaires de flux d’octets inscrits. Éventuellement, un gestionnaire mis en correspondance peut créer la source du média.<br/> Cet indicateur ne peut pas être combiné avec \_ l' \_ indicateur de maintien de la résolution MF du \_ \_ flux \_ d’octets actif \_ en cas d' \_ échec. Pour plus d'informations, consultez la section Notes.<br/> |
| <span id="MF_RESOLUTION_KEEP_BYTE_STREAM_ALIVE_ON_FAIL"></span><span id="mf_resolution_keep_byte_stream_alive_on_fail"></span><dl> <dt>**MF \_ La \_ résolution \_ conserve \_ \_ le flux d’octets actif \_ sur \_ échec**</dt> <dt>0x00000020</dt> </dl>                                                                             | Si la résolution de la source échoue, le programme de résolution source ne ferme pas le flux d’octets. Par défaut, le programme de résolution source ferme le flux d’octets en cas d’échec.<br/> Si cet indicateur est utilisé et que la résolution de la source échoue, l’appelant doit à nouveau appeler la méthode et définir le \_ contenu de résolution MF \_ ne doit \_ \_ pas \_ nécessairement \_ correspondre à l' \_ extension ou à l’indicateur de \_ \_ \_ \_ type MIME.<br/> Cet indicateur ne peut pas être combiné avec le \_ contenu de résolution MF \_ \_ ne \_ \_ doit pas nécessairement \_ correspondre à l' \_ extension ou à l’indicateur de \_ \_ \_ \_ type MIME. Pour plus d'informations, consultez la section Notes.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="MF_RESOLUTION_READ"></span><span id="mf_resolution_read"></span><dl> <dt>**MF \_ RÉSOLUTION de \_ lecture**</dt> <dt>0x00010000</dt> </dl>                                                                                                                                                                | Demande l’accès en lecture à la source.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MF_RESOLUTION_WRITE"></span><span id="mf_resolution_write"></span><dl> <dt>**MF \_ 0x00020000 \_ écriture de résolution**</dt> <dt></dt> </dl>                                                                                                                                                             | Demande l’accès en écriture à la source.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="MF_RESOLUTION_DISABLE_LOCAL_PLUGINS"></span><span id="mf_resolution_disable_local_plugins"></span><dl> <dt>**MF \_ RÉSOLUTION \_ désactiver \_ les \_ plug-ins locaux**</dt> <dt>0x00000040</dt> </dl>                                                                                                           | Le programme de résolution source n’utilisera pas les plug-ins du schéma inscrit localement ou du gestionnaire ByteStream.<br/> Requiert Windows 8.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="remarks"></a>Remarques

L’application définit ces indicateurs quand elle utilise l’interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) . Le programme de résolution source transmet les mêmes indicateurs aux méthodes [**IMFByteStreamHandler :: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) et [**IMFSchemeHandler :: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject) .

Vous devez spécifier l’un des \_ \_ indicateurs BYTESTREAM de résolution MF ou MF \_ \_ . Les indicateurs restants sont tous facultatifs.

L' \_ indicateur de \_ maintien \_ du \_ flux d’octets actif de la résolution MF en cas \_ \_ \_ d’échec est défini pour le scénario suivant :

1.  L’application tente d’ouvrir une source sur le réseau. L’application définit l' \_ \_ indicateur de maintien de la résolution MF du \_ \_ flux d’octets \_ actif en cas \_ d' \_ échec.

2.  L’URL de la source contient une extension de nom de fichier incorrecte. Étant donné que l’extension de nom de fichier est incorrecte, le gestionnaire de flux d’octets par défaut ne peut pas créer la source du média. Étant donné que l’application a défini l' \_ \_ \_ indicateur de conservation du flux d’octets actif de la résolution MF en cas \_ \_ \_ d' \_ échec, le programme de résolution source met en cache le flux d’octets.

3.  Le programme de résolution source renvoie un code d’erreur à l’application.

4.  Le client ouvre à nouveau la source. cette fois, la définition du \_ \_ contenu de résolution MF ne doit \_ \_ pas \_ nécessairement \_ correspondre à l' \_ extension ou à l’indicateur de \_ \_ \_ \_ type MIME. Cet indicateur force le programme de résolution source à essayer tous les gestionnaires inscrits au lieu du gestionnaire par défaut uniquement. Étant donné que le flux d’octets a été mis en cache, le programme de résolution de source n’a pas besoin d’ouvrir à nouveau le flux d’octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes Media Foundation](media-foundation-constants.md)
</dt> <dt>

[**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
</dt> <dt>

[**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)
</dt> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> <dt>

[Résolveur source](source-resolver.md)
</dt> </dl>

 

 




