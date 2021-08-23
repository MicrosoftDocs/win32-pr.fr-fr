---
description: La méthode Configure doit être implémentée par le moniteur. Le MCSVC appelle cette méthode pour obtenir les informations de configuration de la capture.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: IMonitor ::D méthode oConfigure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 9776ca62cbb61b6708f00d5e1d6d85eeab245b32798683b5afde546d835633c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779189"
---
# <a name="imonitordoconfigure-method"></a>IMonitor ::D méthode oConfigure

La méthode **configure** doit être implémentée par le moniteur. Le MCSVC appelle cette méthode pour obtenir les informations de configuration de la capture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Nom d’une instance du moniteur.

</dd> <dt>

*pConfiguration* \[ dans\]
</dt> <dd>

Chaîne de configuration fournie par MCSVC. L’analyse doit analyser cette chaîne pour les données de configuration.

</dd> <dt>

*ppScriptInstance* \[ à\]
</dt> <dd>

Adresse de la chaîne HTML utilisée pour configurer l’analyse. Si un script par défaut est utilisé pour la configuration, cette valeur doit être définie sur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est \_ OK (ce qui correspond à la même erreur) et MCSVC exécute l’analyse.

Si la méthode échoue, la valeur de retour est un code d’erreur. Une valeur de retour de \_ la configuration de l’analyseur de NMERR \_ \_ a échoué, mais lorsque cette erreur est retournée, le moniteur ne peut pas démarrer tant qu’un appel de **configuration** ultérieure n’a pas réussi. Toute autre erreur empêche l’activation de l’instance du moniteur.

## <a name="remarks"></a>Remarques

Le MCSVC appelle cette méthode une fois qu’il s’est connecté au réseau et avant l’appel de la méthode [IRTC :: configure](irtc-configure.md) .

Le moniteur peut stocker les informations fournies par cet appel, mettre à jour le script HTML ou la chaîne de configuration, et définir le [filtre de capture](capture-filters.md) dans l’objet BLOB NPP.

Le MCSVC peut appeler cette méthode plusieurs fois, mais il ne peut pas être appelé pendant que l’analyse capture des données. Notez que chaque fois qu’un [NPP](network-packet-providers.md) démarre une capture, la connexion au réseau doit être configurée. Cette restriction comprend les situations dans lesquelles le NPP démarre et arrête la même capture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




