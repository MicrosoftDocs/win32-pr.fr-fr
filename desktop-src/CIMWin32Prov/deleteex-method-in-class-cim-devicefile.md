---
description: Méthode DeleteEx de la classe CIM_DeviceFile-la méthode DeleteEx supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode Delete et est héritée de la \_ LOGICALFILE CIM.
ms.assetid: ef4d08cd-7287-47be-bcfc-edc248ac5c9b
ms.tgt_platform: multiple
title: Méthode DeleteEx de la classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e21fb57558d7704bf98740de8634bc91289e0038
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089596"
---
# <a name="deleteex-method-of-the-cim_devicefile-class"></a>Méthode DeleteEx de la \_ classe CIM DeviceFile

La méthode **DeleteEx** supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode [**Delete**](delete-method-in-class-cim-devicefile.md) et est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StopFileName* \[ à\]
</dt> <dd>

Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué. Ce paramètre a la valeur null si la méthode est réussie.

</dd> <dt>

*StartFileName* \[ dans\]
</dt> <dd>

Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode. En règle générale, le paramètre **StartFileName** est le paramètre **StopFileName** spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent. Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

[\_DEVICEFILE CIM](deleteex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**\_DEVICEFILE CIM**](cim-devicefile.md)
</dt> </dl>

 

