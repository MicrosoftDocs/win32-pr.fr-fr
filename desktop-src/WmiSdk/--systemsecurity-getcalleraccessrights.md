---
description: Définit le paramètre rights en tant que bitmap avec chaque bit correspondant à un droit d’accès.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Méthode GetCallerAccessRights de la classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 770a4a51a6a0ea9e38e8c5bd6fed944b473a41373933cee497e98fd8f9952422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110024"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a>Méthode GetCallerAccessRights de la \_ \_ classe SystemSecurity

La méthode **\_ \_ SystemSecurity :: GetCallerAccessRights** définit le paramètre *Rights* comme une image bitmap avec chaque bit correspondant à un droit d’accès. N’importe quel client peut l’appeler pour déterminer les droits dont dispose le client. Cette méthode est utile pour les clients qui activent ou désactivent des fonctionnalités. Par exemple, une application GUI peut désactiver un bouton si l’utilisateur actuellement connecté ne dispose pas des droits d’exécution de méthode.

Tout client activé a le droit d’appeler **GetCallerAccessRights**, même si ce client ne dispose pas des droits d’exécution de méthode généraux.

## <a name="syntax"></a>Syntaxe


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*droits* \[ à\]
</dt> <dd>

Droits d’accès du client. Pour plus d’informations, consultez [**\_ \_ SystemSecurity**](--systemsecurity.md) et [constantes de sécurité WMI](wmi-security-constants.md).

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ ACTIVER** (1 (0x1))


</dt> <dd>

Active le compte et accorde des autorisations de lecture à l’utilisateur. Il s’agit du droit d’accès par défaut pour tous les utilisateurs.

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ MÉTHODE \_ Execute** (2 (0X2))


</dt> <dd>

Autorise l’exécution des méthodes.

> [!Note]  
> Les fournisseurs peuvent effectuer des vérifications d’accès supplémentaires.

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ \_ \_ REP en écriture complète** (4 (0x4))


</dt> <dd>

Permet à l’appelant, au contexte de sécurité ou à l’utilisateur d’écrire dans les classes et les instances, à l’exception des classes système.

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ \_ \_ REP en écriture partielle** (8 (0x8))


</dt> <dd>

Permet à l’appelant, au contexte de sécurité ou à l’utilisateur d’écrire des instances de fournisseur, mais pas des classes statiques ou des instances statiques dans le référentiel.

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ \_Fournisseur d’écriture** (16 (0x10))


</dt> <dd>

Permet à l’appelant, au contexte de sécurité ou à l’utilisateur d’écrire des classes et des instances sur les fournisseurs.

> [!Note]  
> L’emprunt d’identité des fournisseurs peut effectuer des vérifications d’accès supplémentaires.

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ \_Accès à distance** (32 (0x20))


</dt> <dd>

Permet à un compte d’utilisateur d’effectuer à distance les opérations autorisées par les autres bits.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Lecture \_ CONTRÔLE** (131072 (0x20000))


</dt> <dd>

Autorise l’accès en lecture aux descripteurs de sécurité.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Écriture \_ DAC** (262144 (0x40000))


</dt> <dd>

Autorise l’accès en écriture à des listes de contrôle d’accès discrétionnaire (DACL).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un **HRESULT** qui indique l’état de l’appel de la méthode. La liste suivante répertorie les valeurs de retour dont l’importance est de [**Set9XUserList**](--systemsecurity-set9xuserlist.md). pour les applications de script et de Visual Basic, le résultat peut être obtenu à partir de out- [parameters. ReturnValue](parsing-outparameters-objects.md). Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**\_méthode WBEM \_ E \_ désactivée**
</dt> <dd>

Cette méthode n’est pas prise en charge sur les versions prises en charge de Windows.

</dd> </dl>

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



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

[Constantes de sécurité WMI](wmi-security-constants.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sécurisation des espaces de noms WMI](securing-wmi-namespaces.md)
</dt> <dt>

Constantes de sécurité WMI
</dt> </dl>

 

