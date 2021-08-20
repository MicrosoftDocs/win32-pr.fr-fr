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
ms.openlocfilehash: 7685ce1f1c9c7d8f519395c578000375742eea49dd169085e99c582e14c35a29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143710"
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



 

## <a name="remarks"></a>Remarques

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



 

 




