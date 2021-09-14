---
description: La méthode ProvideTextData est appelée par Mergemod.dll pour récupérer des données de texte à partir de l’outil client. Mergemod.dll fournit le nom à partir de l’entrée correspondante dans la table ModuleConfiguration.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: Méthode ConfigureModule. ProvideTextData (Mergemod. h)
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
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091997"
---
# <a name="configuremoduleprovidetextdata-method"></a>Méthode ConfigureModule. ProvideTextData

La méthode **ProvideTextData** est appelée par Mergemod.dll pour récupérer des données de texte à partir de l’outil client. Mergemod.dll fournit le *nom* à partir de l’entrée correspondante dans la table ModuleConfiguration.

L’outil doit retourner S \_ OK et fournir le texte de personnalisation approprié dans ConfigData. L’outil client est chargé d’allouer les données, mais Mergemod. dllis est responsable de la libération de la mémoire. Cet argument doit être un objet **BSTR** . **LPCWSTR** n’est pas accepté.

Si l’outil ne fournit pas de données de configuration pour cette valeur de *nom* , la fonction doit retourner S \_ false. Dans ce cas Mergemod.dll ignore la valeur de l’argument ConfigData et utilise la valeur par défaut de la table ModuleConfiguration.

Tout code de retour autre que S \_ OK ou s \_ false entraîne la journalisation d’une erreur (si un journal est ouvert) et entraîne l’échec de la fusion.

Étant donné que cette fonction suit la convention **BSTR** standard, NULL est équivalent à la chaîne vide.

## <a name="syntax"></a>Syntaxe


```JScript
ConfigureModule.ProvideTextData(
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

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le client peut être appelé plusieurs fois pour chaque enregistrement de la [table ModuleConfiguration](moduleconfiguration-table.md). Notez que Mergemod.dll n’effectue jamais plusieurs appels au client pour la même valeur « Name ». Si aucun enregistrement de la table ModuleSubstitution n’utilise la propriété, une entrée de la table ModuleConfiguration n’entraîne aucun appel au client.

### <a name="c"></a>C++

Consultez [**fonction ProvideTextData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




