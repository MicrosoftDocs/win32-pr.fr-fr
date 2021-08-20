---
description: La méthode ProvideIntegerData de l’objet ConfigureModule est appelée par Mergemod.dll pour récupérer des données de type entier à partir de l’outil client.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Méthode ConfigureModule. ProvideIntegerData (Mergemod. h)
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
ms.openlocfilehash: 96472a13902322d940dc7e756c3639f9befaf6764b3ede8521f27a885a50e8d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143688"
---
# <a name="configuremoduleprovideintegerdata-method"></a>Méthode ConfigureModule. ProvideIntegerData

La méthode **ProvideIntegerData** de l' [**objet ConfigureModule**](configuremodule-object.md) est appelée par Mergemod.dll pour récupérer des données de type entier à partir de l’outil client.

Mergemod.dll fournit le *nom* à partir de l’entrée correspondante dans la [table ModuleConfiguration](moduleconfiguration-table.md).

L’outil doit retourner S \_ OK et fournir l’entier de personnalisation approprié dans *ConfigData*.

Si l’outil ne fournit pas de données de configuration pour cette valeur de *nom* , la fonction doit retourner S \_ false. Dans ce cas Mergemod.dll ignore la valeur de l’argument *ConfigData* et utilise la valeur par défaut de la table ModuleConfiguration.

## <a name="syntax"></a>Syntaxe


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* 
</dt> <dd>

Nom de l’élément pour lequel les données sont récupérées.

</dd> <dt>

*ConfigData* 
</dt> <dd>

Pointeur vers le texte de personnalisation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le client peut être appelé plusieurs fois pour chaque enregistrement de la [table ModuleConfiguration](moduleconfiguration-table.md). Notez que Mergemod.dll n’effectue jamais plusieurs appels au client pour la même valeur « Name ». Si aucun enregistrement de la table ModuleSubstitution n’utilise la propriété, une entrée de la table ModuleConfiguration n’entraîne aucun appel au client.

### <a name="c"></a>C++

Consultez [**fonction ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




