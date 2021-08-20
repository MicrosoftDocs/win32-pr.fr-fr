---
description: Obtient le descripteur de sécurité pour l’espace de noms auquel l’utilisateur est connecté. Cette méthode retourne un descripteur de sécurité au format de tableau d’octets binaire. Si vous écrivez un script, utilisez la méthode GetSecurityDescriptor.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Obtient la méthode de la classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 720443358cfce776dfe02630ea25ea994ad0ef552a9d89627b2f136e990e0194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109987"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a>Méthode d’obtient de la \_ \_ classe SystemSecurity

La méthode **obtient** le descripteur de sécurité pour l’espace de noms auquel l’utilisateur est connecté. Cette méthode retourne un descripteur de sécurité au format de tableau d’octets binaire. Si vous écrivez un script, utilisez la méthode [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) . Pour plus d’informations, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md) et [modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md).

L’utilisateur doit disposer de l’autorisation de **\_ contrôle de lecture** . Par défaut, les administrateurs disposent de cette autorisation. La seule partie du descripteur de sécurité qui est réellement utilisée est la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List). La liste DACL peut contenir à la fois des ACE héritées et non héritées. Les ACE Deny et allow sont autorisées.

Si vous programmez en C++, vous pouvez manipuler le descripteur de sécurité binaire à l’aide de [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)et des méthodes de conversion [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) et [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="syntax"></a>Syntaxe


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SD* \[ à\]
</dt> <dd>

Descripteur de sécurité au format de tableau d’octets binaire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un **HRESULT** indiquant l’état de l’appel de la méthode. La liste suivante répertorie les valeurs de retour dont l’importance **est déconseillée.** pour les applications de script et de Visual Basic, le résultat peut être obtenu à partir de out- [parameters. ReturnValue](parsing-outparameters-objects.md). Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**\_OK**
</dt> <dd>

Méthode exécutée avec succès.

</dd> <dt>

**\_accès WBEM \_ E \_ refusé**
</dt> <dd>

L’appelant ne dispose pas des droits suffisants pour appeler cette méthode.

</dd> <dt>

**\_méthode WBEM \_ E \_ désactivée**
</dt> <dd>

Tentative d’exécution de cette méthode sur un système non pris en charge.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour plus d’informations sur la modification de la sécurité des espaces de noms par programmation ou manuelle, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md).

## <a name="examples"></a>Exemples

Le script suivant vous montre comment utiliser l'  objet pour obtenir le descripteur de sécurité actuel de l' \\ espace de noms Cimv2 racine et le remplacer par le tableau d’octets affiché dans la propriété distante.


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



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

[Constantes de sécurité WMI](wmi-security-constants.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_\_SystemSecurity :: SetS**](--systemsecurity-setsd.md)
</dt> <dt>

[**Descripteur de sécurité \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sécurisation des espaces de noms WMI](securing-wmi-namespaces.md)
</dt> </dl>

 

