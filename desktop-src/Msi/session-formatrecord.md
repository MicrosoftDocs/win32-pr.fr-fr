---
description: La méthode FormatRecord de l’objet session retourne une chaîne mise en forme à partir d’un modèle et des données d’enregistrement.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Session. FormatRecord, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007316"
---
# <a name="sessionformatrecord-method"></a>Session. FormatRecord, méthode

La méthode **FormatRecord** de l’objet [**session**](session-object.md) retourne une chaîne mise en forme à partir d’un modèle et des données d’enregistrement.

## <a name="syntax"></a>Syntaxe


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*enregistrement* 
</dt> <dd>

Objet **Record** requis contenant un modèle et des données à mettre en forme. La chaîne de modèle doit être définie dans le champ 0, suivi de tous les paramètres de données référencés.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode **FormatRecord** utilise le processus de format suivant.

Les paramètres à mettre [en forme](formatted.md) sont placés entre crochets \[ .. \] . Les crochets peuvent être itérés, car les substitutions sont résolues de l’intérieur vers l’extérieur.

Si une partie de la chaîne est entourée d’accolades {} et ne contient aucun crochet, la partie reste inchangée, y compris les accolades.

Si une partie de la chaîne est placée entre accolades et contient un ou plusieurs noms de propriété, et si toutes les propriétés sont trouvées, le texte (avec les substitutions résolues) s’affiche sans les accolades. Si l’une des propriétés est introuvable, tout le texte entre les accolades et les accolades elles-mêmes sont supprimés.

**Pour mettre en forme des chaînes à l’aide de la méthode FormatRecord**

1.  Les paramètres numériques sont remplacés en remplaçant le marqueur par la valeur du champ d’enregistrement correspondant, avec des valeurs manquantes ou null qui ne génèrent pas de texte.
2.  La chaîne résultante est traitée en remplaçant les paramètres non-enregistrement par les valeurs correspondantes, comme indiqué dans les descriptions suivantes.
    -   Si une sous-chaîne se présentant sous la forme « \[ PropertyName \] » est rencontrée, elle est remplacée par la valeur de la propriété.
    -   Si une sous-chaîne du formulaire « \[ % EnvironmentVariable \] » est trouvée, la valeur de la variable d’environnement est remplacée.
    -   Si une sous-chaîne du formulaire \[ \# *filekey* \] est trouvée, elle est remplacée par le chemin d’accès complet du fichier, avec la valeur *filekey* utilisée comme clé dans la [table de fichiers](file-table.md). La valeur de \[ \# *filekey* \] reste vide et n’est pas remplacée par un chemin d’accès jusqu’à ce que le programme d’installation exécute l’action [CostInitialize](costinitialize-action.md), l’action [FileCost](filecost-action.md)et l' [action CostFinalize](costfinalize-action.md). La valeur de \[ \# *filekey* \] dépend de l’état d’installation du composant auquel le fichier appartient. Si le composant est exécuté à partir de la source, la valeur est le chemin d’accès à l’emplacement source du fichier. Si le composant est exécuté localement, la valeur est le chemin d’accès à l’emplacement cible du fichier après l’installation. Si le composant est absent, le chemin d’accès est vide. Pour plus d’informations sur la vérification de l’état d’installation des composants, consultez [vérification de l’installation de fonctionnalités, de composants et de fichiers](checking-the-installation-of-features-components-files.md).
    -   Si une sous-chaîne du formulaire \[ *$componentkey* \] est trouvée, elle est remplacée par le répertoire d’installation du composant, avec la valeur *componentkey* utilisée comme clé dans la [table des composants](component-table.md). La valeur de \[ $ *componentkey* \] reste vide et n’est pas remplacée par un répertoire tant que le programme d’installation n’a pas exécuté l’action [CostInitialize](costinitialize-action.md), l’action [FileCost](filecost-action.md)et l' [action CostFinalize](costfinalize-action.md). La valeur de \[ $ *componentkey* \] dépend de l’état d’installation du composant. Si le composant est exécuté à partir de la source, la valeur est le répertoire source du fichier. Si le composant est exécuté localement, la valeur est le répertoire cible après l’installation. Si le composant est absent, la valeur est laissée vide. Pour plus d’informations sur la vérification de l’état d’installation des composants, consultez [vérification de l’installation de fonctionnalités, de composants et de fichiers](checking-the-installation-of-features-components-files.md).
    -   Si une sous-chaîne du formulaire « \[ \\ c \] » est trouvée, elle est remplacée par le caractère sans traitement supplémentaire. Seul le premier caractère après la barre oblique inverse est conservé ; tout le reste est supprimé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Correct](formatted.md)
</dt> <dt>

[Types de données de colonne](column-data-types.md)
</dt> </dl>

 

 




