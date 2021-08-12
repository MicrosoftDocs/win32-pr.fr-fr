---
description: Récupère la taille actuelle, en octets, de l’espace d’adressage virtuel libre disponible pour le processus.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Méthode GetAvailableVirtualSize de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7cdea363ce835297469242a4166d5e1e9eeea0845f27d0c780eef88f775bf751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675991"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a>Méthode GetAvailableVirtualSize de la \_ classe de processus Win32

Récupère la taille actuelle, en octets, de l’espace d’adressage virtuel libre disponible pour le processus.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AvailableVirtualSize* \[ à\]
</dt> <dd>

Le paramètre *AvailableVirtualSize* retourne l’espace d’adressage virtuel gratuit disponible pour ce processus.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro (0) pour indiquer la réussite de l’opération. Tout autre nombre indique une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Opération réussie**
</dt> <dd>

0

L’opération s’est terminée avec succès.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

L’utilisateur n’a pas accès aux informations demandées

</dd> <dt>

**Privilège insuffisant**
</dt> <dd>

3

L’utilisateur ne dispose pas de privilèges suffisants.

</dd> <dt>

**Échec inconnu**
</dt> <dd>

8

Échec inconnu.

</dd> <dt>

**Chemin d'accès introuvable**
</dt> <dd>

9

Le chemin d'accès spécifié n'existe pas.

</dd> <dt>

**Paramètre non valide**
</dt> <dd>

21

Le paramètre spécifié n’est pas valide.

</dd> <dt>

**Autres**
</dt> <dd>

22 4294967295

Pour les valeurs autres que celles listées, reportez-vous à la documentation sur les [codes d’erreur système](/windows/desktop/Debug/system-error-codes) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                       |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Processus Win32**](win32-process.md)
</dt> </dl>

 

