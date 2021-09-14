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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011663"
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



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

