---
title: Interface INapSoHProcessor (NapProtocol. h)
description: Sont utilisés par les Sha pour traiter le contenu de SoHResponses et par les validateurs d’intégrité du système pour traiter le contenu de SoHRequests.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- NAP de l’interface INapSoHProcessor
- INapSoHProcessor interface NAP, Description
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c43abf137bb267468deeb9d4bd47546275ba6c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032384"
---
# <a name="inapsohprocessor-interface"></a>Interface INapSoHProcessor

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

**INapSoHProcessor** fournit des méthodes utilisées par les Sha pour traiter le contenu de [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) et par les validateurs d’intégrité du système pour traiter le contenu de **SoHRequests**.

## <a name="members"></a>Membres

L’interface **INapSoHProcessor** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSoHProcessor** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapSoHProcessor** possède ces méthodes.



| Méthode                                                                                           | Description                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md)         | Recherche l’index d’emplacement de l’attribut de paquet SoH suivant.<br/>                 |
| [**INapSoHProcessor :: GetAttribute**](inapsohprocessor-getattribute-method.md)                   | Récupère le type et la valeur de l’attribut.<br/>                                    |
| [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md) | Récupère le nombre d’attributs contenus dans la SoH.<br/>                   |
| [**INapSoHProcessor :: Initialize**](inapsohprocessor-initialize-method.md)                       | Initialise le paquet de protocole SoH et le système NAP pour le traitement du contenu.<br/> |



 

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

 

