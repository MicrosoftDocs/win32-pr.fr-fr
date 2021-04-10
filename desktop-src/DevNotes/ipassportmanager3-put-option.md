---
description: Définit une option de connexion Microsoft .NET Passport spécifique.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: IPassportManager3 ::p méthode ut_Option
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 52a1324c4b1a04a207b5bccac1a95bcd060be8ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950424"
---
# <a name="ipassportmanager3put_option-method"></a>IPassportManager3 ::p \_ méthode d’option ut

Définit une option de connexion Microsoft .NET Passport spécifique.

> [!Note]  
> La méthode **put \_ option** appartient à l’interface [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) . Cette rubrique complète la documentation initiale.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*name* 
</dt> <dd>

Option de connexion à définir. Actuellement, la seule option prise en charge est iMode.

</dd> <dt>

*newVal* 
</dt> <dd>

**Variante** (VT \_ bool) qui spécifie la nouvelle valeur de l’option. Cette valeur peut être true ou false.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne \_ la valeur OK lorsque la méthode est réussie.

## <a name="remarks"></a>Notes

Cette méthode est fournie avec les versions antérieures du kit de développement logiciel (SDK) Passport.

 

 
