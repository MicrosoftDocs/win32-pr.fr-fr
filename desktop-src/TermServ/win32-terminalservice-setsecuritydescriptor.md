---
title: Méthode SetSecurityDescriptor de la classe Win32_Service (Services Bureau à distance)
description: Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès au service.
ms.assetid: 4F03B798-0912-4A0D-B31E-419662D5849B
ms.tgt_platform: multiple
keywords:
- Windows Management Instrumentation de script, sécurité
- Windows Management Instrumentation de sécurité, scripts
- Services Bureau à distance de la méthode SetSecurityDescriptor
- Services Bureau à distance de la méthode SetSecurityDescriptor, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode SetSecurityDescriptor
topic_type:
- apiref
api_name:
- Win32_Service.SetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a21f9730b4c1c0ab7b3ccf662ddb2d95da2ee2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743485"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a>Méthode SetSecurityDescriptor de la classe Win32_Service (Services Bureau à distance)

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

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

La demande a été acceptée.

</dd> <dt>

**1**
</dt> <dd>

La demande n'est pas prise en charge.

</dd> <dt>

**2**
</dt> <dd>

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

Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**** La propriété State) est égale à 0, 1 ou 2.

</dd> <dt>

**6**
</dt> <dd>

Le service n'a pas été démarré.

</dd> <dt>

**7**
</dt> <dd>

Le service n'a pas répondu à la demande de démarrage en temps voulu.

</dd> <dt>

**8**
</dt> <dd>

Échec inconnu lors du démarrage du service.

</dd> <dt>

**9**
</dt> <dd>

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

**21**
</dt> <dd>

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
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dt>

[**Constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modification de la sécurité d’accès sur les objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

