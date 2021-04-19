---
description: L’objet ConfigureModule est une interface implémentée par le client.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Objet ConfigureModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531104"
---
# <a name="configuremodule-object"></a>Objet ConfigureModule

L' **objet ConfigureModule** est une interface implémentée par le client. Mergemod.dllappelle des méthodes sur l’interface **IMsmConfigureModule** pour demander que l’outil client fournisse des informations de configuration. Le module est configuré en fonction des réponses du client aux appels sur cette interface.

## <a name="members"></a>Membres

L’objet **ConfigureModule** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **ConfigureModule** a ces méthodes.



| Méthode                                                           | Description                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**ProvideIntegerData**](configuremodule-provideintegerdata.md) | Appelée par Mergemod.dll pour obtenir des entiers utilisés pour configurer le module.<br/> |
| [**ProvideTextData**](configuremodule-providetextdata.md)       | Appelée par Mergemod.dll pour obtenir le texte utilisé pour configurer le module.<br/>     |



 

## <a name="remarks"></a>Notes

### <a name="c"></a>C++

interface **IMsmConfigureModule : IDispatch**

### <a name="interface-id"></a>ID d’interface



| Constante                     | Valeur                                  |
|------------------------------|----------------------------------------|
| **IID \_ IMsmConfigureModule** | {AC013209-18A7-4851-8A21-2353443D70A0} |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




