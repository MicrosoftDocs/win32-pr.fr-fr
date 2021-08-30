---
title: IMsRdpClientNonScriptable6, interface
description: fournit l’accès aux propriétés qui ne sont pas scriptables de la session à distance d’un client sur le contrôle Bureau à distance ActiveX. Dérive de l’interface IMsRdpClientNonScriptable5.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable6
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable6, Description
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 6beede518b346ff4934730eb6fa8c3ed9f80dec980be031f9d09e774aeb359a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033219"
---
# <a name="imsrdpclientnonscriptable6-interface"></a>IMsRdpClientNonScriptable6, interface

fournit l’accès aux propriétés qui ne sont pas scriptables de la session à distance d’un client sur le contrôle Bureau à distance ActiveX. Dérive de l’interface [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) . Les méthodes de cette interface sont accessibles uniquement par le biais de la vtable ; ils ne peuvent pas être utilisés pour des clients scriptables.

Une instance de cette interface est obtenue en appelant [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet [**IMsTscAx**](imstscax-interface.md) , en passant **IID \_ IMsRdpClientNonScriptable6**.

## <a name="members"></a>Membres

L’interface **IMsRdpClientNonScriptable6** hérite de [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md). **IMsRdpClientNonScriptable6** a également les types de membres suivants :

- [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpClientNonScriptable6** possède ces méthodes.


| Méthode            | Description                   |
|:-----------------------------|:-----------------|
| [**SendLocation2D**](imsrdpclientnonscriptable6-sendlocation2d.md)     |  Envoie une valeur de latitude et de longitude au serveur afin que l’emplacement géographique du client puisse être reflété dans la session à distance.                   |
| [**SendLocation3D**](imsrdpclientnonscriptable6-sendlocation3d.md)     | Envoie une valeur de latitude, de longitude et d’altitude au serveur afin que l’emplacement géographique du client puisse être reflété dans la session à distance.                 |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1709 (build 16299)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | Le CLSID \_ MsRdpClient12 est défini en tant que 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> Le CLSID \_ MsRdpClient12NotSafeForScripting est défini en tant que 3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> Le CLSID \_ MsRdpClient11 est défini en tant que 22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> Le CLSID \_ MsRdpClient11NotSafeForScripting est défini en tant que 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable6 est défini comme 05293249-B28B-4db8-BE64-1B2F496B910E            |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>
