---
description: Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’espace de noms WMI auquel vous êtes connecté. Le descripteur de sécurité est représenté par une instance de \_ \_ SecurityDescriptor.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: Méthode SetSecurityDescriptor de la classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: fcdc192801b839451cee256f57090780818d2046
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921828"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Méthode SetSecurityDescriptor de la \_ \_ classe SystemSecurity

La méthode [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’espace de noms WMI auquel vous êtes connecté. Le descripteur de sécurité est représenté par une instance de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md). Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Descripteur* \[ dans\]
</dt> <dd>

Descripteur de sécurité associé à l’espace de noms WMI.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur. Pour plus d’informations, consultez [codes de retour WMI](wmi-return-codes.md) ou [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**0**
</dt> <dd>

Achèvement réussi.

</dd> <dt>

**2**
</dt> <dd>

L’utilisateur n’a pas accès aux informations demandées.

</dd> <dt>

**8**
</dt> <dd>

Échec inconnu.

</dd> <dt>

**9**
</dt> <dd>

L’utilisateur ne dispose pas des privilèges suffisants pour exécuter la méthode.

</dd> <dt>

**21**
</dt> <dd>

Un paramètre spécifié dans l’appel de méthode n’est pas valide.

</dd> </dl>

## <a name="remarks"></a>Notes

L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de Access Control système*](/windows/desktop/SecGloss/a-gly) (SACL). Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).

Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné. Pour plus d’informations, consultez [**constantes de privilège**](privilege-constants.md) et [exécution d’opérations privilégiées](executing-privileged-operations.md).

Vous pouvez mettre à jour la liste DACL et la liste SACL dans l’instance [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) lors de l’appel de cette méthode, mais vous pouvez également mettre à jour uniquement la liste DACL ou uniquement la liste SACL.

Les valeurs suivantes dans [**le \_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) déterminent si la liste DACL ou la liste SACL ou les deux sont mises à jour.

-   **SE \_ liste DACL \_ présente**

    Indique que la liste DACL doit être mise à jour. Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste DACL.

-   **SE \_ liste SACL \_ présente**

    Indique que la liste SACL doit être mise à jour. Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste SACL. Pour mettre à jour la liste SACL, le privilège **SeSecurityPrivilege** doit être activé sur le compte. Pour les scripts, le nom du privilège est **SeSecurityPrivilege**. Pour plus d’informations, consultez [**constantes de privilège**](privilege-constants.md).

Si les propriétés tiers de confiance du groupe et tiers de confiance du propriétaire ne sont pas **null**, elles sont mises à jour. Dans le cas contraire, WMI conserve les valeurs d’origine. Pour plus d’informations, consultez [objets descripteurs de sécurité WMI](wmi-security-descriptor-objects.md).

Quand une nouvelle SACL a la **valeur null** dans un appel de cette méthode, le descripteur de sécurité SACL de l’objet sécurisable cible reste inchangé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> </dl>

 

