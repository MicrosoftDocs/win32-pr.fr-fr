---
title: Interface IMsRdpDrive
description: Contient des informations sur un objet lecteur.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDrive
- Services Bureau à distance de l’interface IMsRdpDrive, Description
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 032e62ca54d6adccce9b27c8f7e95160c800759b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739989"
---
# <a name="imsrdpdrive-interface"></a>Interface IMsRdpDrive

Contient des informations sur un objet lecteur.

## <a name="members"></a>Membres

L’interface **IMsRdpDrive** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDrive** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpDrive** possède les propriétés suivantes.



| Propriété                                                            | Type d’accès           | Description                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Nom**](imsrdpdrive-name.md)<br/>                         | Lecture seule<br/>  | Récupère le nom du lecteur.<br/>              |
| [**RedirectionState**](imsrdpdrive-redirectionstate.md)<br/> | Lecture/écriture<br/> | Indique l’état de redirection du lecteur.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDrive est défini en tant que d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

