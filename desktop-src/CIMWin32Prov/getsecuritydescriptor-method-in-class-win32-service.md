---
description: Méthode GetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)-retourne le descripteur de sécurité qui contrôle l’accès au service.
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Méthode GetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c19f22cf57a811a7caebfbcc9bf4202c8d2ad7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095098"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Méthode GetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)

La méthode **GetSecurityDescriptor** retourne le descripteur de sécurité qui contrôle l’accès au service. Le descripteur est retourné sous la forme d’une instance de l’expression [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Descripteur* \[ à\]
</dt> <dd>

Descripteur de sécurité associé au service.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

La demande a été acceptée.

</dd> <dt>


</dt> <dd>

1

La demande n'est pas prise en charge.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

L’utilisateur n’a pas l’accès nécessaire.

</dd> <dt>


</dt> <dd>

3

Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.

</dd> <dt>


</dt> <dd>

4

Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.

</dd> <dt>


</dt> <dd>

5

Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).**** La propriété State) est égale à 0, 1 ou 2.

</dd> <dt>


</dt> <dd>

6

Le service n'a pas été démarré.

</dd> <dt>


</dt> <dd>

7

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


</dt> <dd>

10

Le service est déjà en cours d'exécution.

</dd> <dt>


</dt> <dd>

11

La base de données pour ajouter un nouveau service est verrouillée.

</dd> <dt>


</dt> <dd>

12

Une dépendance sur laquelle repose ce service a été supprimée du système.

</dd> <dt>


</dt> <dd>

13

Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.

</dd> <dt>


</dt> <dd>

14

Le service a été désactivé du système.

</dd> <dt>


</dt> <dd>

15

Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.

</dd> <dt>


</dt> <dd>

16

Ce service est en cours de suppression du système.

</dd> <dt>


</dt> <dd>

17

Le service n’a pas de thread d’exécution.

</dd> <dt>


</dt> <dd>

18

Le service a des dépendances circulaires lorsqu’il démarre.

</dd> <dt>


</dt> <dd>

19

Un service est en cours d’exécution sous le même nom.

</dd> <dt>


</dt> <dd>

20

Le nom du service contient des caractères non valides.

</dd> <dt>

**Paramètre non valide**
</dt> <dd>

21

Des paramètres non valides ont été transmis au service.

</dd> <dt>


</dt> <dd>

22

Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.

</dd> <dt>


</dt> <dd>

23

Le service existe dans la base de données des services disponibles dans le système.

</dd> <dt>


</dt> <dd>

24

Le service est actuellement mis en pause dans le système.

</dd> <dt>

**Autres**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="remarks"></a>Notes

L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL). Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).

Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné. Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Exemples

Lorsque vous récupérez un descripteur de sécurité dans VBScript, veillez à « sécurité » et à exécuter en tant qu’administrateur, comme illustré dans l’extrait de code suivant. Dans le cas contraire, votre code risque de générer une erreur d’autorisation.


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



de même, dans VB .net, veillez à définir « EnablePrivileges = True » et à exécuter l’Application en tant qu’administrateur.


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a>Spécifications



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

 

