---
title: ISoftKbd Initialize, méthode (Softkbdc. h)
description: La méthode Initialize ISoftKbd initialise tous les champs nécessaires pour un clavier logiciel et génère des dispositions de clavier souples standard.
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Initialiser la méthode Text Services Framework
- Initialiser la méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, Initialize, méthode
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311250"
---
# <a name="isoftkbdinitialize-method"></a>ISoftKbd :: Initialize, méthode

La méthode **ISoftKbd :: Initialize** initialise tous les champs nécessaires pour un clavier conditionnel et génère des dispositions de clavier souples standard.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Initialize();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                | Description                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





