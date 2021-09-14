---
description: La méthode CompressEx compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode Compress. Cette méthode est héritée de la \_ LOGICALFILE CIM.
ms.assetid: a5f7b35b-5d52-4129-bf7e-6db5e0ff6852
ms.tgt_platform: multiple
title: Méthode CompressEx de la classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e607497a8bb49d0a5926e5b50eb3310c671d9f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920508"
---
# <a name="compressex-method-of-the-cim_devicefile-class"></a>Méthode CompressEx de la \_ classe CIM DeviceFile

La méthode **CompressEx** compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode [**Compress**](compress-method-in-class-cim-devicefile.md) . Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 CompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StopFileName* \[ à\]
</dt> <dd>

Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué. Ce paramètre a la **valeur null** si la méthode est réussie.

</dd> <dt>

*StartFileName* \[ dans\]
</dt> <dd>

Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode. En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier (ou le répertoire) auquel une erreur s’est produite à partir de l’appel de méthode précédent. Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Récursif* \[ dans\]
</dt> <dd>

Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ DeviceFile**](cim-devicefile.md) . Pour les instances de fichier, ce paramètre est ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.

<dl> <dt>


</dt> <dd>

0

Réussite.

</dd> <dt>


</dt> <dd>

2

Accès refusé.

</dd> <dt>


</dt> <dd>

8

Échec non spécifié.

</dd> <dt>


</dt> <dd>

9

Objet non valide.

</dd> <dt>


</dt> <dd>

10

L’objet existe déjà.

</dd> <dt>


</dt> <dd>

11

Le système de fichiers n’est pas NTFS.

</dd> <dt>


</dt> <dd>

12

Plateforme non Windows.

</dd> <dt>


</dt> <dd>

13

Le lecteur n’est pas le même.

</dd> <dt>


</dt> <dd>

14

le répertoire n'est pas vide.

</dd> <dt>


</dt> <dd>

15

Violation de partage.

</dd> <dt>


</dt> <dd>

16

Fichier de démarrage non valide.

</dd> <dt>


</dt> <dd>

17

Privilège non détenu.

</dd> <dt>


</dt> <dd>

21

Paramètre non valide.

</dd> </dl>

## <a name="remarks"></a>Notes

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

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

[\_DEVICEFILE CIM](compressex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**\_DEVICEFILE CIM**](cim-devicefile.md)
</dt> </dl>

 

