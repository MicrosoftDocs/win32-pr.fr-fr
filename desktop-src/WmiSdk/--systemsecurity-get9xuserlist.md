---
description: Obtient les droits d’accès à distance pour une liste d’utilisateurs individuels sur des ordinateurs exécutant des versions obsolètes de Windows, où le contrôle d’accès via les descripteurs de sécurité Windows n’est pas disponible.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: '__SystemSecurity :: Get9XUserList, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530151"
---
# <a name="__systemsecurityget9xuserlist-method"></a>\_\_SystemSecurity :: Get9XUserList, méthode

La méthode [**\_ \_ SystemSecurity :: Set9XUserList**](--systemsecurity-set9xuserlist.md) obtient les droits d’accès à distance pour une liste d’utilisateurs individuels sur des ordinateurs exécutant des versions obsolètes de Windows, où le contrôle d’accès par le biais de descripteurs de sécurité Windows n’est pas disponible.

Cette fonction est similaire au descripteur de sécurité, mais elle est plus limitée. Les groupes ne sont pas pris en charge et il n’y a aucun contrôle sur l’accès local, car l’utilisateur local a toujours un accès complet. Refuser et autoriser les entrées de contrôle d’accès (ACE) sont autorisées, et pour cette raison, l’ordre d’accès est important dans la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List). Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UL* \[ à\]
</dt> <dd>

Tableau d’utilisateurs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un **HRESULT** qui indique l’état de l’appel de la méthode. La liste suivante répertorie les valeurs de retour dont l’importance est de **Get9XUserList**. Pour les scripts et les applications de Visual Basic, le résultat peut être [Parameters. returnValue](parsing-outparameters-objects.md). Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**\_méthode WBEM \_ E \_ désactivée**
</dt> <dd>

Cette méthode n’est pas prise en charge sur les versions prises en charge de Windows.

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

 

