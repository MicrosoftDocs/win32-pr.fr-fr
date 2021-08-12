---
title: Méthode StopService de la classe Win32_Service (Sdoias. h) (service Terminal Server)
description: Place le service, représenté par l' \_ objet Win32 TerminalService, à l’état arrêté.
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- Méthode StopService Services Bureau à distance
- Méthode StopService Services Bureau à distance, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode StopService
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4edbdb9e3b7fa48476f70e550bf1255de344880df440381fcd48adefa2f68d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604359"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a>Méthode StopService de la classe Win32_Service (Sdoias. h) pour le service Terminal Server

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** place le service, représenté par l’objet [**Win32 \_ TerminalService**](win32-terminalservice.md) , à l’état arrêté.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 StopService();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

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

## <a name="remarks"></a>Remarques

Une fois que vous avez déterminé quels services peuvent être arrêtés ou suspendus, vous pouvez utiliser les méthodes **StopService** et [**PauseService**](win32-terminalservice-pauseservice.md) pour arrêter et suspendre les services. La décision d’arrêter un service plutôt que de le suspendre, ou vice versa, dépend de plusieurs facteurs, notamment les suivants :

-   Le service est-il susceptible d’être suspendu ? Si ce n’est pas le cas, la seule option consiste à arrêter le service.
-   Avez-vous besoin de continuer à gérer les demandes des clients pour quiconque déjà connecté au service ? Dans ce cas, la suspension d’un service lui permet généralement de gérer les clients existants tout en refusant l’accès aux nouveaux clients. En revanche, lorsque vous arrêtez un service, tous les clients sont immédiatement déconnectés.
-   Avez-vous besoin de reconfigurer un service et de faire en sorte que les modifications prennent effet immédiatement ? Bien que les propriétés de service puissent être modifiées pendant l’interruption d’un service, la plupart d’entre elles ne prennent pas effet tant que le service n’est pas arrêté et redémarré.

Le code de script requis pour arrêter un service est presque identique au code requis pour suspendre le service.

Si vous tentez d’arrêter un service qui a des services dépendants en cours d’exécution, la méthode **StopService** échoue avec une valeur de retour de 3. Les services dépendants doivent d’abord être arrêtés.

Si vous arrêtez un service, vérifiez immédiatement le [**\_ TerminalService Win32**](win32-terminalservice.md).**Propriété State** , car la valeur peut toujours afficher le service comme étant en cours d’exécution.

## <a name="examples"></a>Exemples

[L’ensemble de RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) L’exemple PowerShell définit l’état du service pour les ordinateurs distants.

L’exemple [d’arrêt d’un service et de ses dépendants](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript arrête un service et tous les services dépendants.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| En-tête<br/>                   | <dl> <dt>Sdoias. h</dt> </dl>     |
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

[**PauseService**](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 

