---
title: Interface INapSoHConstructor (NapProtocol. h)
description: Sont utilisés par l’SHA pour construire SoHRequests et par les programmes de validation d’intégrité système pour construire SoHResponses.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- NAP de l’interface INapSoHConstructor
- INapSoHConstructor interface NAP, Description
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941729"
---
# <a name="inapsohconstructor-interface"></a>Interface INapSoHConstructor

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

**INapSoHConstructor** fournit des méthodes qui sont utilisées par l’SHA pour construire des [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) et par les validateurs d’intégrité du système pour construire **SoHResponses**.

## <a name="members"></a>Membres

L’interface **INapSoHConstructor** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSoHConstructor** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapSoHConstructor** possède ces méthodes.



| Méthode                                                                                   | Description                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [**INapSoHConstructor::AppendAttribute**](inapsohconstructor-appendattribute-method.md) | Ajoute un TLV à la fin de la mémoire tampon SoH.<br/> |
| [**INapSoHConstructor::GetSoH**](inapsohconstructor-getsoh-method.md)                   | Récupère le paquet SoH construit.<br/>    |
| [**INapSoHConstructor :: Initialize**](inapsohconstructor-initialize-method.md)           | Initialise le paquet SoH.<br/>              |
| [**INapSoHConstructor :: Validate**](inapsohconstructor-validate-method.md)               | Vérifie la validité du paquet SoH.<br/>   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

