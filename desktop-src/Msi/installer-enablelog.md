---
description: La méthode EnableLog de l’objet installer active la journalisation du type de message sélectionné pour toutes les sessions d’installation suivantes dans l’espace de processus actuel.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Installer. EnableLog, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 48481a701b7e78de372f5579dab5c9d5976a68063958b0812d6ae1ddc08b109a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631695"
---
# <a name="installerenablelog-method"></a>Installer. EnableLog, méthode

La méthode **EnableLog** de l’objet [**installer**](installer-object.md) active la journalisation du type de message sélectionné pour toutes les sessions d’installation suivantes dans l’espace de processus actuel.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*logMode* 
</dt> <dd>

Chaîne obligatoire qui contient des lettres représentant les types de messages à consigner. La chaîne peut être une combinaison des valeurs suivantes.



| Valeur | Description                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| I     | Messages d’information uniquement.                                                                             |
| w     | Messages d’avertissement non récupérables.                                                                            |
| e     | Messages d’erreur pouvant être des erreurs irrécupérables.                                                               |
| f     | Liste des fichiers en cours d’utilisation qui doivent être remplacés.                                                         |
| a     | Début de la notification d’action.                                                                          |
| r     | Enregistrement de données d’action contenant du contenu spécifique à l’action.                                              |
| u     | Messages de demande de l’utilisateur.                                                                                 |
| c     | Paramètres d’initialisation de l’interface utilisateur.                                                                          |
| m     | Message d’insuffisance de mémoire.                                                                                 |
| v     | L’envoi de grandes quantités d’informations au fichier journal n’est généralement pas utile aux utilisateurs. Peut être utilisé pour la prise en charge. |
| p     | Table des propriétés de vidage ; « property = value » à l’arrêt du moteur                                          |
| \+    | Ajouter au fichier journal existant.                                                                           |
| !     | Videz chaque ligne dans le fichier journal.                                                                       |
| x     | Informations supplémentaires sur le débogage. cette option est disponible uniquement avec Windows Server 2003.                      |
| o     | Messages d’espace disque insuffisants.                                                                            |



 

</dd> <dt>

*Relog* 
</dt> <dd>

Chaîne obligatoire contenant le chemin d’accès au fichier journal à créer. Utilisez une chaîne vide ("") pour désactiver la journalisation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le chemin d’accès à l’emplacement du fichier journal doit déjà exister lors de l’utilisation de cette méthode. Le programme d’installation ne crée pas la structure de répertoire pour le fichier journal.

les options de journalisation définies à l’aide de **EnableLog** remplacent les paramètres de stratégie de journalisation Windows Installer existants.

La journalisation remplace un fichier journal existant par défaut. Vous devez utiliser la lettre « + » dans le mode de journalisation pour ajouter à un fichier journal existant.

L’option' ! 'n’est pas recommandée, car elle peut ralentir considérablement l’installation. Cette option peut être utile lors du débogage d’une installation.

L’exemple de script suivant active la journalisation documentée pour une installation. À la fin de l’installation, le fichier journal généré se trouve dans c : \\ temp \\ install. log.


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Journalisation du programme d’installation](windows-installer-logging.md)
</dt> </dl>

 

 




