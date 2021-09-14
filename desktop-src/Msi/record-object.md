---
description: L’objet record est un conteneur destiné à contenir et à transférer un nombre variable de valeurs.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Objet record
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009722"
---
# <a name="record-object"></a>Objet record

L’objet **Record** est un conteneur destiné à contenir et à transférer un nombre variable de valeurs. Les champs de l’enregistrement sont indexés numériquement et peuvent contenir des chaînes, des entiers, des objets et des valeurs NULL. Les champs au-delà de la taille des enregistrements alloués sont traités comme ayant des valeurs null de manière permanente. Le champ numéro 0 est réservé.

## <a name="members"></a>Membres

L’objet **Record** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **Record** possède ces méthodes.



| Méthode                                  | Description                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**ClearData**](record-cleardata.md)   | Efface les données de tous les champs, en leur affectant la valeur null.<br/>                                      |
| [**FormatText**](record-formattext.md) | Met en forme les champs en fonction du modèle dans le champ 0.<br/>                                      |
| [**ReadStream**](record-readstream.md) | Lit un nombre spécifié d’octets à partir d’un champ d’enregistrement contenant les données de flux.<br/>                |
| [**SetStream**](record-setstream.md)   | Copie le contenu du fichier spécifié dans le champ d’enregistrement désigné en tant que données de flux.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **Record** possède ces propriétés.



| Propriété                                             | Type d’accès           | Description                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**DataSize**](record-datasize.md)<br/>       |                       | Retourne la taille des données pour le champ désigné.<br/>                             |
| [**FieldCount**](record-fieldcount.md)<br/>   |                       | Retourne le nombre de champs dans l'enregistrement.<br/>                                        |
| [**IntegerData**](record-integerdata.md)<br/> | Lecture/écriture<br/> | Transfère les données de type entier 32 bits dans ou en dehors d’un champ spécifié dans l’enregistrement.<br/> |
| [**IsNull**](record-isnull.md)<br/>           |                       | Retourne la valeur true si le champ indiqué est null et false si le champ contient des données.<br/>  |
| [**StringData**](record-stringdata.md)<br/>   | Lecture/écriture<br/> | Transfère les données de chaîne dans ou en dehors d’un champ spécifié dans l’enregistrement.<br/>         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode CreateRecord**](installer-createrecord.md)
</dt> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




