---
description: Méthode SetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)-écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès au service.
ms.assetid: c1745b69-f355-4b4c-9e58-6a76c230f498
ms.tgt_platform: multiple
title: Méthode SetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20619a459171841d0a3bd5b7acabe984dc835dac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100003"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Méthode SetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)

La méthode **SetSecurityDescriptor** écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès au service.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Descripteur* \[ dans\]
</dt> <dd>

Descripteur de sécurité associé au service.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

La demande a été acceptée.

</dd> <dt>

**1**
</dt> <dd>

La demande n'est pas prise en charge.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

L’utilisateur n’a pas l’accès nécessaire.

</dd> <dt>

**3**
</dt> <dd>

Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.

</dd> <dt>

**4**
</dt> <dd>

Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.

</dd> <dt>

**5**
</dt> <dd>

Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).**** La propriété State) est égale à 0, 1 ou 2.

</dd> <dt>

**6**
</dt> <dd>

Le service n'a pas été démarré.

</dd> <dt>

**7**
</dt> <dd>

Le service n'a pas répondu à la demande de démarrage en temps voulu.

</dd> <dt>

**Échec inconnu**
</dt> <dd>

8

Échec inconnu lors du démarrage du service.

</dd> <dt>

**Privilège manquant**
</dt> <dd>

9

Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.

</dd> <dt>

**10**
</dt> <dd>

Le service est déjà en cours d'exécution.

</dd> <dt>

**11**
</dt> <dd>

La base de données pour ajouter un nouveau service est verrouillée.

</dd> <dt>

**12**
</dt> <dd>

Une dépendance sur laquelle repose ce service a été supprimée du système.

</dd> <dt>

**13**
</dt> <dd>

Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.

</dd> <dt>

**14**
</dt> <dd>

Le service a été désactivé du système.

</dd> <dt>

**15**
</dt> <dd>

Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.

</dd> <dt>

**16**
</dt> <dd>

Ce service est en cours de suppression du système.

</dd> <dt>

**17**
</dt> <dd>

Le service n’a pas de thread d’exécution.

</dd> <dt>

**19**
</dt> <dd>

Le service a des dépendances circulaires lorsqu’il démarre.

</dd> <dt>

**19**
</dt> <dd>

Un service est en cours d’exécution sous le même nom.

</dd> <dt>

**20**
</dt> <dd>

Le nom du service contient des caractères non valides.

</dd> <dt>

**Paramètre non valide**
</dt> <dd>

21

Des paramètres non valides ont été transmis au service.

</dd> <dt>

**22**
</dt> <dd>

Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.

</dd> <dt>

**23**
</dt> <dd>

Le service existe dans la base de données des services disponibles dans le système.

</dd> <dt>

**24**
</dt> <dd>

Le service est actuellement mis en pause dans le système.

</dd> <dt>

**Autre**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="remarks"></a>Notes 

L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL). Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).

Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné. Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).

Vous pouvez mettre à jour la liste DACL et la liste SACL dans l’instance [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) lors de l’appel de cette méthode, mais vous pouvez également mettre à jour uniquement la liste DACL ou uniquement la liste SACL.

Les valeurs suivantes dans [**le \_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) déterminent si la liste DACL, la liste SACL ou les deux sont mises à jour.

-   **SE \_ DACL en \_ présence**

    Indique que la liste DACL doit être mise à jour. Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste DACL.

-   **\_liste SACL se \_ présente**

    Indique que la liste SACL doit être mise à jour. Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste SACL. Pour mettre à jour la liste SACL, le privilège **SeSecurityPrivilege** doit être activé sur le compte. Pour les scripts, le nom du privilège est **SeSecurityPrivilege**. Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants).

Si les propriétés tiers de confiance du groupe et tiers de confiance du propriétaire ne sont pas **null**, elles sont mises à jour. Dans le cas contraire, WMI conserve les valeurs d’origine. Pour plus d’informations, consultez [objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).

Quand une nouvelle SACL a la **valeur null** dans un appel de cette méthode, le descripteur de sécurité SACL de l’objet sécurisable cible reste inchangé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service Win32**](win32-service.md)
</dt> <dt>

[**Constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modification de la sécurité d’accès sur les objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

