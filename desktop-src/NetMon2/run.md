---
description: L’expert doit implémenter la fonction Run. Moniteur réseau appelle la fonction Run pour démarrer l’expert au sein de la DLL de l’expert.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Exécuter une fonction de rappel (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: e31c5c729bba133fa4c4d3e36bbc54035a274923a03a8718acf05a601192775b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074499"
---
# <a name="run-callback-function"></a>Exécuter une fonction de rappel

L’expert doit implémenter la fonction **Run** . Moniteur réseau appelle la fonction **Run** pour démarrer l’expert au sein de la dll de l’expert.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hExpertKey* \[ dans\]
</dt> <dd>

Identificateur unique de l’expert qui est passé à toutes les fonctions Moniteur réseau spécifiques à l’expert.

> [!Note]  
> L’identificateur *hExpertKey* peut passer une clé d’expert qui est différente de la clé d’expert que la fonction de [**configuration**](configure.md) passe.

 

</dd> <dt>

*pConfig* \[ dans\]
</dt> <dd>

Pointeur vers la configuration existante. Le paramètre *pConfig* peut avoir la **valeur null** , ce qui signifie que l’expert peut s’exécuter avec des valeurs par défaut codées en dur, ou des informations de démarrage auxquelles le paramètre *pExpertStartupInfo* fait référence.

</dd> <dt>

*pExpertStartupInfo* \[ dans\]
</dt> <dd>

Pointeur vers l’élément de capture qui a le focus au démarrage de l’expert.

</dd> <dt>

*StartupFlags* \[ dans\]
</dt> <dd>

Indicateur de la façon dont l’expert doit utiliser le paramètre *pExpertStartupInfo* .

Le seul indicateur défini est :



| Valeur                                                                                                                                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <dt>**l' \_ indicateur de démarrage expert \_ utilise les données de \_ \_ démarrage sur les données de \_ \_ \_ configuration \_ .**</dt> </dl> | Cet indicateur indique que l’expert utilise le paramètre *pExpertStartupInfo* et n’utilise pas le paramètre *pConfig* . En règle générale, vous pouvez définir cet indicateur lorsque l’expert peut démarrer à partir d’un clic avec la souris. Si l’indicateur n’est pas défini, les deux éléments suivants peuvent se produire : l’expert ne démarre pas à partir d’un clic droit, ou l’expert commence à partir d’un clic avec la souris, puis l’utilisateur le configure.<br/> |



 

</dd> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Le paramètre *HWND* du parent (généralement l’interface utilisateur Moniteur réseau).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit (autrement dit, si l’expert démarre), la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Remarques

Lors de son exécution, l’expert parcourt les frames du fichier de capture et génère un rapport ou crée des événements qui présentent des problèmes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




