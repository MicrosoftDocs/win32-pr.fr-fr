---
description: définit les droits d’accès à distance pour une liste d’utilisateurs individuels sur des ordinateurs exécutant des versions obsolètes de Windows, où le contrôle d’accès via Windows descripteurs de sécurité n’est pas disponible.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: '__SystemSecurity :: Set9XUserList, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: d1185fa91d9d12e240f592d458b975b650947cf5b8cd1b289a7e016b455556a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109960"
---
# <a name="__systemsecurityset9xuserlist-method"></a>\_\_SystemSecurity :: Set9XUserList, méthode

la méthode **\_ \_ SystemSecurity :: Set9XUserList** définit les droits d’accès à distance pour une liste d’utilisateurs individuels sur les ordinateurs qui exécutent des versions obsolètes de Windows, où le contrôle d’accès via Windows descripteurs de sécurité n’est pas disponible.

La liste est spécifiée sous la forme d’un tableau d’objets incorporés où chaque objet est une instance de la classe [**\_ \_ NTLMUser9X**](--ntlmuser9x.md) . Cette fonction est similaire au descripteur de sécurité, mais elle est plus limitée. Les groupes ne sont pas pris en charge et il n’y a aucun contrôle sur l’accès local, car l’utilisateur local a toujours un accès complet. Refuser et autoriser les entrées de contrôle d’accès (ACE) sont autorisées, et pour cette raison, l’ordre d’accès est important dans la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List). Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UL* \[ dans\]
</dt> <dd>

Tableau d’utilisateurs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un **HRESULT** qui indique l’état de l’appel de la méthode. La liste suivante répertorie les valeurs de retour dont l’importance est de **Set9XUserList**. pour les applications de script et de Visual Basic, le résultat peut être obtenu à partir de out- [parameters. ReturnValue](parsing-outparameters-objects.md). Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**\_méthode WBEM \_ E \_ désactivée**
</dt> <dd>

Cette méthode n'est pas prise en charge.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity :: est**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity :: SetS**](--systemsecurity-setsd.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sécurisation des espaces de noms WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Constantes de sécurité WMI](wmi-security-constants.md)
</dt> </dl>

 

