---
description: Arrête le service représenté par l’objet dérivé de Win32 \_ BaseService.
ms.assetid: 5d6427a6-d233-4db4-9235-c6187b36da5f
ms.tgt_platform: multiple
title: Méthode StopService de la classe Win32_BaseService (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5b31b854255c6b20253875233bf2e5a44207a5a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513142"
---
# <a name="stopservice-method-of-the-win32_baseservice-class"></a>Méthode StopService de la \_ classe BaseService Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** arrête le service représenté par l’objet dérivé de [**Win32 \_ BaseService**](win32-baseservice.md).

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 StopService();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.

<dl> <dt>

**Success**
</dt> <dd>

0

La demande a été acceptée.

</dd> <dt>

**Non pris en charge**
</dt> <dd>

1

La demande n'est pas prise en charge.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

L’utilisateur n’a pas l’accès nécessaire.

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

Le code de contrôle demandé ne peut pas être envoyé au service, car l’état du service (propriété de l'[**État**](win32-baseservice.md) de [**\_ BaseService Win32**](win32-baseservice.md)) est égal à 0, 1 ou 2.

</dd> <dt>

**Service non actif**
</dt> <dd>

6

Le service n'a pas été démarré.

</dd> <dt>

**Délai d’expiration de la demande de service**
</dt> <dd>

7

Le service n'a pas répondu à la demande de démarrage en temps voulu.

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

Une dépendance sur laquelle repose ce service a été supprimée du système.

</dd> <dt>

**Échec de la dépendance du service**
</dt> <dd>

13

Le service n’a pas pu trouver le service nécessaire à partir d’un service dépendant.

</dd> <dt>

**Service désactivé**
</dt> <dd>

14

Le service a été désactivé du système.

</dd> <dt>

**Échec de l’ouverture de session du service**
</dt> <dd>

15

Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.

</dd> <dt>

**Service marqué pour suppression**
</dt> <dd>

16

Ce service est en cours de suppression du système.

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

Des paramètres non valides ont été transmis au service.

</dd> <dt>

**Compte de service de l’état non valide**
</dt> <dd>

22

Le compte sous lequel ce service doit s’exécuter n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.

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
| En-tête<br/>                   | <dl> <dt>Sdoias. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_BaseService Win32**](win32-baseservice.md)
</dt> </dl>

 

