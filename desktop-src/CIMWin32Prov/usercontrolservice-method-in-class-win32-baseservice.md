---
description: Tente d’envoyer un code de contrôle défini par l’utilisateur à un service.
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: Méthode UserControlService de la classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861598"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a>Méthode UserControlService de la \_ classe Win32 BaseService

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) tente d’envoyer un code de contrôle défini par l’utilisateur à un service.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ControlCode* \[ dans\]
</dt> <dd>

Valeur qui spécifie une commande de contrôle pour un service. Par exemple, une commande de contrôle est une commande « suspendre » ou « continuer ». La valeur peut être un code prédéfini, ou une valeur et une action que le service définit. Les codes de contrôle prédéfinis sont les suivants :

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**\_le contrôle du service \_ continue**


</dt> <dd>

Avertit un service suspendu de reprendre.

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**interrogation du contrôle des services \_ \_**


</dt> <dd>

Avertit un service qu’il doit signaler les informations d’état actuelles au gestionnaire de contrôle des services.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**\_NETBINDADD de contrôle de service \_**


</dt> <dd>

Notifie un service réseau qu’il existe un nouveau composant pour la liaison.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**\_NETBINDDISABLE de contrôle de service \_**


</dt> <dd>

Notifie un service réseau qu’une de ses liaisons est désactivée.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**\_NETBINDENABLE de contrôle de service \_**


</dt> <dd>

Notifie un service réseau qu’une liaison désactivée est activée.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**\_NETBINDREMOVE de contrôle de service \_**


</dt> <dd>

Notifie un service réseau qu’un composant pour la liaison a été supprimé.

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**\_PARAMCHANGE de contrôle de service \_**


</dt> <dd>

Avertit un service que ses paramètres de démarrage sont modifiés.

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**\_suspension du contrôle de service \_**


</dt> <dd>

Notifie un service de s’interrompre.

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**\_arrêt du contrôle de service \_**


</dt> <dd>

Notifie l’arrêt d’un service.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.

<dl> <dt>

**Success**
</dt> <dd>

0

La demande est acceptée.

</dd> <dt>

**Non pris en charge**
</dt> <dd>

1

La demande n'est pas prise en charge.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

L’utilisateur ne dispose pas des droits d’accès nécessaires.

</dd> <dt>

**Services dépendants en cours d’exécution**
</dt> <dd>

3

Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.

</dd> <dt>

**Contrôle de service non valide**
</dt> <dd>

4

Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.

</dd> <dt>

**Le service ne peut pas accepter le contrôle**
</dt> <dd>

5

Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).**** La propriété State) est égale à 0, 1 ou 2.

</dd> <dt>

**Service non actif**
</dt> <dd>

6

Ce service n'a pas démarré.

</dd> <dt>

**Délai d’expiration de la demande de service**
</dt> <dd>

7

Le service ne répond pas rapidement à la demande de démarrage.

</dd> <dt>

**Échec inconnu**
</dt> <dd>

8

Processus interactif.

</dd> <dt>

**Chemin introuvable**
</dt> <dd>

9

Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.

</dd> <dt>

**Service déjà en cours d’exécution**
</dt> <dd>

10

Le service est déjà en cours d'exécution.

</dd> <dt>

**Base de données du service verrouillée**
</dt> <dd>

11

La base de données pour ajouter un nouveau service est verrouillée.

</dd> <dt>

**Dépendance de service supprimée**
</dt> <dd>

12

Une dépendance sur laquelle repose ce service est supprimée du système.

</dd> <dt>

**Échec de la dépendance du service**
</dt> <dd>

13

Le service ne trouve pas le service nécessaire à partir d’un service dépendant.

</dd> <dt>

**Service désactivé**
</dt> <dd>

14

Le service est désactivé du système.

</dd> <dt>

**Échec de l’ouverture de session du service**
</dt> <dd>

15

Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.

</dd> <dt>

**Service marqué pour suppression**
</dt> <dd>

16

Le service est en cours de suppression du système.

</dd> <dt>

**Service sans thread**
</dt> <dd>

17

Il n'y a pas de thread d'exécution pour le service.

</dd> <dt>

**Dépendance circulaire d’État**
</dt> <dd>

18

Le démarrage du service donne lieu à des dépendances circulaires.

</dd> <dt>

**Nom de l’État en double**
</dt> <dd>

19

Un service est en cours d'exécution sous le même nom.

</dd> <dt>

**Nom de l’état non valide**
</dt> <dd>

20

Le nom du service contient des caractères non valides.

</dd> <dt>

**Paramètre d’État non valide**
</dt> <dd>

21

Des paramètres non valides ont été passés au service.

</dd> <dt>

**Compte de service de l’état non valide**
</dt> <dd>

22

Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.

</dd> <dt>

**Le service d’État existe**
</dt> <dd>

23

Le service existe dans la base de données des services disponibles dans le système.

</dd> <dt>

**Service déjà suspendu**
</dt> <dd>

24

Le service est actuellement mis en pause dans le système.

</dd> <dt>

**Autres**
</dt> <dd>

25 4294967295

</dd> </dl>

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

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_BaseService Win32**](win32-baseservice.md)
</dt> </dl>

 

