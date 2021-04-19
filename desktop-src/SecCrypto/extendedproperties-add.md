---
description: Ajoute une propriété étendue à la collection.
ms.assetid: 1d6b3c39-17b0-4a7c-a5c2-4a3bd866be07
title: ExtendedProperties. Add, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06e4170b34dcdca97bc0bae6bb48b4a057a8e9b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543241"
---
# <a name="extendedpropertiesadd-method"></a>ExtendedProperties. Add, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler la fonction API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et obtenir les propriétés. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

La méthode **Add** ajoute une propriété étendue à la collection.

## <a name="syntax"></a>Syntaxe


```VB
ExtendedProperties.Add( _
  ByVal valProperty _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valProperty* \[ dans\]
</dt> <dd>

Objet [**ExtendedProperty**](extendedproperty.md) qui représente la propriété étendue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
