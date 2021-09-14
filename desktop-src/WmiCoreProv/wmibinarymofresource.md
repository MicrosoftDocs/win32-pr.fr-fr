---
description: Le fournisseur de classes WDM définit la classe WMIBinaryMofResource dans \\ l' \\ espace de noms WMI racine pour prendre en charge la tâche de suivi de l’état des données dans l’espace de stockage WMI.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: WMIBinaryMofResource, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013098"
---
# <a name="wmibinarymofresource-class"></a>WMIBinaryMofResource, classe

Le fournisseur de classes WDM définit la classe **WMIBinaryMofResource** dans \\ l' \\ espace de noms WMI racine pour prendre en charge la tâche de suivi de l’état des données dans l’espace de stockage WMI.

## <a name="syntax"></a>Syntaxe

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a>Membres

La classe **WMIBinaryMofResource** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **WMIBinaryMofResource** possède les propriétés suivantes.

<dl> <dt>

**HighDateTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Moitié supérieure de l’horodatage.

</dd> <dt>

**LowDateTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Moitié inférieure de l’horodatage.

</dd> <dt>

**MofProcessed**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indicateur précisant si le fichier. mof a été entièrement traité.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Nom du pilote compatible WDM pour lequel un fichier MOF binaire a été compilé avec succès dans l’espace de stockage WMI.

</dd> </dl>

## <a name="remarks"></a>Notes

Le fournisseur de classes WDM crée une instance de **WMIBinaryMofResource** pour chaque pilote WDM qui fournit un fichier MOF binaire.

Chaque fois que WMI Initialise le fournisseur, le fournisseur compare l’horodatage avec l’horodateur du fichier image du pilote. Si les horodateurs diffèrent, WMI RECOMPILE le fichier MOF.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2003<br/>                                                     |
| Espace de noms<br/>                | \\WMI racine<br/>                                                               |
| MOF<br/>                      | <dl> <dt>WMI. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fournisseur WDM](wdm-provider.md)
</dt> </dl>

 

