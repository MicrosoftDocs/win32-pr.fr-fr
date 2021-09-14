---
title: Méthode PauseService de la classe Win32_Service (Services Bureau à distance)
description: 'Méthode PauseService de la classe Win32_Service (Services Bureau à distance) : tente de placer le service dans l’état suspendu.'
ms.assetid: 101987F6-FBAB-4E79-B1FA-346B1EF58DE1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode PauseService
- Services Bureau à distance de la méthode PauseService, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode PauseService
topic_type:
- apiref
api_name:
- Win32_Service.PauseService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c9847f363d9bc6d1743da6189d2c4290c00dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856750"
---
# <a name="pauseservice-method-of-the-win32_service-class-remote-desktop-services"></a>Méthode PauseService de la classe Win32_Service (Services Bureau à distance)

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** tente de placer le service dans l’état suspendu.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 PauseService();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

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

Une fois que vous avez déterminé quels services peuvent être arrêtés ou suspendus, vous pouvez utiliser les méthodes [**StopService**](win32-terminalservice-stopservice.md) et **PauseService** pour arrêter et suspendre les services. La décision d’arrêter un service plutôt que de le suspendre, ou vice versa, dépend de plusieurs facteurs, notamment les suivants :

-   Le service est-il susceptible d’être suspendu ? Si ce n’est pas le cas, la seule option consiste à arrêter le service.
-   Avez-vous besoin de continuer à gérer les demandes des clients pour quiconque déjà connecté au service ? Dans ce cas, la suspension d’un service lui permet généralement de gérer les clients existants tout en refusant l’accès aux nouveaux clients. En revanche, lorsque vous arrêtez un service, tous les clients sont immédiatement déconnectés.
-   Avez-vous besoin de reconfigurer un service et de faire en sorte que les modifications prennent effet immédiatement ? Bien que les propriétés de service puissent être modifiées pendant l’interruption d’un service, la plupart d’entre elles ne prennent pas effet tant que le service n’est pas arrêté et redémarré.

Le code de script requis pour arrêter un service est presque identique au code requis pour suspendre le service.

## <a name="examples"></a>Exemples

L’exemple de [suspension de services s’exécutant sous un compte spécifique](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) met en pause tous les services qui s’exécutent sous le compte de service hypothétique netsvc.

## <a name="requirements"></a>Spécifications



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

[Classes du système d’exploitation](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dt>

[Tâches WMI : services](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)
</dt> </dl>

 

