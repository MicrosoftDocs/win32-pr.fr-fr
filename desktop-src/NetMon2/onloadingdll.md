---
description: Charge la DLL du moniteur.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: OnLoadingDLL, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6049684798d6dda9030abd667c28a62f4b19f9b4e66a831ef4c1d2caa880fb1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676869"
---
# <a name="onloadingdll-function"></a>OnLoadingDLL fonction)

La fonction **OnLoadingDLL** charge la dll de l’analyse.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFilterBlob* \[ in, out\]
</dt> <dd>

Objet BLOB utilisé par le MCSVC pour correspondre à une analyse avec des cartes réseau disponibles. Ce paramètre contient toujours une demande pour une interface [IRTC](irtc.md) . la plupart des analyses n’ont donc pas besoin d’ajouter d’entrées à l’objet BLOB. Toutefois, une analyse personnalisée peut ajouter des critères de filtre supplémentaires (par exemple, si le type MAC doit être Ethernet).

</dd> <dt>

*pCreateFlags* \[ dans\]
</dt> <dd>

Indicateurs qui indiquent comment le MCSVC contrôle la création d’une analyse. Ce paramètre doit avoir l’une des valeurs suivantes :



| Valeur                                                                                                                                                                                                            | Signification                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <dt>**MCS \_ créer \_ un \_ par \_ carte réseau**</dt> </dl>          | Le MCSVC garantit qu’une seule instance de ce moniteur existe pour chaque carte réseau. Une deuxième instance peut être créée uniquement si la première est détruite.<br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <dt>**MCS- \_ créer \_ \_ des configurations par \_ défaut**</dt> </dl> | Si le moniteur a une configuration interne par défaut, MCSVC ne demande pas à l’utilisateur de configurer le moniteur avant la création de l’instance.<br/>  |



 

</dd> <dt>

*ppDefaultName* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers l’adresse du nom par défaut de l’analyse. Le MCSVC utilise le nom par défaut lors de la création d’instances de l’analyse.

Par exemple, si le nom par défaut retourné est « moniteur de routeur », la première instance de l’analyse serait « moniteur de routeur 1 », la deuxième « RouterMonitor2 », et ainsi de suite. Si la **valeur null** est retournée, MCSVC utilise le nom de la dll.

</dd> <dt>

*ppDescription* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers l’adresse de la description de l’analyse. La description est transmise à l’outil de contrôle de l’analyse, qui utilise la description pour indiquer à l’utilisateur que le moniteur existe. Ce paramètre peut retourner la **valeur null**.

</dd> <dt>

*ppDefaultScript* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers l’adresse du script de formulaire HTML par défaut utilisé pour configurer l’analyse. Bien que les instances du moniteur puissent modifier leur propre script, la plupart des analyses chargent simplement leur script une seule fois, à partir d’un fichier. La valeur de *ppDefaultScript* peut être **null**. Toutefois, soit le moniteur ne peut pas être configuré en externe, soit il doit fournir un script ultérieurement. Il est plus efficace de fournir un script par défaut ici.

</dd> <dt>

*ppDefaultConfig* \[ à\]
</dt> <dd>

Adresse de la chaîne par défaut utilisée pour configurer l’analyse lors de sa création. Ce paramètre peut avoir la valeur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est S OK, ce \_ qui est identique à l’erreur.

Si la fonction échoue, le MCSVC omet le moniteur spécifié dans toutes ses listes ; après, aucune analyse de ce type ne peut être créée.

## <a name="remarks"></a>Remarques

La fonction **OnLoadingDLL** est appelée une fois par MCSVC, lors du premier chargement de la dll. La DLL fournit ensuite les valeurs par défaut qui seront utilisées par le MCSVC lors de la création d’une instance d’analyse.

L’analyse doit allouer toute la mémoire nécessaire pour les chaînes retournées à MCSVC. Au retour, le MCSVC crée des copies de toutes les chaînes et ne tente pas de libérer les chaînes retournées.

Le moniteur doit utiliser les fonctions d’assistance de BLOB pour modifier l’objet BLOB de filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




