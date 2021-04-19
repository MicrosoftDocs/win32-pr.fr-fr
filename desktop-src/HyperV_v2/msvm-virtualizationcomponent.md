---
description: Représente un service de la plateforme Microsoft Windows Hyper-V.
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Classe Msvm_VirtualizationComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19811b224a4e93e85420539248b7d010491335aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514989"
---
# <a name="msvm_virtualizationcomponent-class"></a>MSVM \_ VirtualizationComponent, classe

Représente un service de la plateforme Microsoft Windows Hyper-V.

La syntaxe suivante est simplifiée format MOF (MOF).

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualizationComponent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualizationComponent** possède les propriétés suivantes.

<dl> <dt>

**IDENTIFICATEUR**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**GUID** qui représente l’identificateur de classe de l’objet com du service.

</dd> <dt>

**Contexte**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **expérimental**
</dt> </dl>

Contexte dans lequel l’objet nouvellement créé s’exécutera. Cette valeur est passée dans le paramètre *dwClsContext* à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Cette propriété a toujours la valeur 1.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si cette instance est activée et peut être utilisée pour effectuer les demandes des clients ; Sinon, **false**. Cette propriété a toujours la valeur **true**.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Chaîne indépendante du langage qui identifie de façon unique le service. Le format suivant est suggéré pour empêcher les conflits de noms : « version du composant du fournisseur \| \| ». Par exemple, ce nom représente la version 1,0 du composant de port réseau émulé Microsoft : « Microsoft \| EmulatedNetworkPortComponent \| v 1.0 ».

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ VirtualizationComponent** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Fin de la prise en charge des clients<br/>    | Windows 8.1<br/>                                                                                  |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

