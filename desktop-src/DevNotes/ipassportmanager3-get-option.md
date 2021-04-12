---
description: Récupère la valeur d’une option de connexion Microsoft .NET Passport spécifique.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'IPassportManager3 :: get_Option, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392931"
---
# <a name="ipassportmanager3get_option-method"></a>IPassportManager3 :: \_ méthode d’option, méthode

Récupère la valeur d’une option de connexion Microsoft .NET Passport spécifique.

> [!Note]  
> La méthode d' **\_ option d’extraction** appartient à l’interface [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) . Cette rubrique complète la documentation initiale.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom* \[ dans\]
</dt> <dd>

Option de connexion à récupérer. Actuellement, la seule option prise en charge est « iMode ».

</dd> <dt>

*pval* \[ à\]
</dt> <dd>

Pointeur vers un **Variant** (VT \_ bool) qui reçoit la valeur de l’option. Cette valeur peut être true ou false.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne \_ la valeur OK lorsque la méthode est réussie.

## <a name="remarks"></a>Notes

Cette méthode est fournie avec les versions antérieures du kit de développement logiciel (SDK) Passport.

 

 
