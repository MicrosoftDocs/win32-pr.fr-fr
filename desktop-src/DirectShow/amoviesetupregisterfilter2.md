---
description: La fonction AMovieSetupRegisterFilter2 enregistre les mérites, les codes confidentiels et les types de média d’un filtre dans le registre à l’aide de l’interface IFilterMapper2.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: AMovieSetupRegisterFilter2, fonction (DLLSETUP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528826"
---
# <a name="amoviesetupregisterfilter2-function"></a>AMovieSetupRegisterFilter2 fonction)

La fonction **AMovieSetupRegisterFilter2** enregistre les mérites, les codes confidentiels et les types de média d’un filtre dans le registre à l’aide de l’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*psetupdata* 
</dt> <dd>

Pointeur vers les données de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) .

</dd> <dt>

*pIFM2* 
</dt> <dd>

Pointeur vers l’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

</dd> <dt>

*bRegister* 
</dt> <dd>

Valeur indiquant s’il faut inscrire le filtre ; **True** indique que le filtre est inscrit, **false** indique son annulation de son inscription.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

La fonction [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) appelle cette fonction d’assistance pour inscrire un filtre après l’inscription du serveur com.

En règle générale, un filtre utilise [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) et n’appelle pas cette fonction directement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DLLSETUP. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions de configuration des DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




