---
description: La méthode message de l’objet session effectue toutes les opérations de journalisation activées et diffère l’exécution à l’objet gestionnaire d’interface utilisateur associé au moteur. La journalisation peut être activée de manière sélective pour les différents types de messages. Consultez la méthode EnableLog.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session. message, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537893"
---
# <a name="sessionmessage-method"></a>Session. message, méthode

La méthode **message** de l’objet [**session**](session-object.md) effectue toutes les opérations de journalisation activées et diffère l’exécution à l’objet gestionnaire d’interface utilisateur associé au moteur. La journalisation peut être activée de manière sélective pour les différents types de messages. Consultez la méthode [**EnableLog**](installer-enablelog.md) .

Si le champ d’enregistrement 0 contient une chaîne de mise en forme, il est utilisé pour mettre en forme les données dans les autres champs. Sinon, si le message est une erreur, un avertissement ou un message utilisateur, une tentative est faite pour trouver un modèle de message dans la table d’erreurs pour la base de données actuelle à l’aide du numéro d’erreur trouvé dans le champ 1 de l’enregistrement pour les types de messages et les valeurs de retour.

## <a name="syntax"></a>Syntaxe


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*espèces* 
</dt> <dd>

Le paramètre *Kind* doit avoir l’une des valeurs suivantes. Pour afficher une boîte de message avec des boutons et des icônes de type push, calculez la valeur de *genre* en ajoutant les styles de zone de message standard utilisés par [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) et [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) à **msiMessageTypeError**, **msiMessageTypeWarning** ou **msiMessageTypeUser**. Pour plus d’informations, consultez la section Notes ci-dessous.



| Constante                                                                                                                                                                                                                                                                                                                 | Signification                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt> </dl>                     | Arrêt prématuré, risque de manquer de mémoire.<br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt> </dl>                                     | Message d’erreur mis en forme, \[ 1 \] est le numéro de message dans la [table d’erreurs](error-table.md).<br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt> </dl>                             | Message d’avertissement mis en forme, \[ 1 \] est le numéro de message dans la [table d’erreurs](error-table.md).<br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <dt> **msiMessageTypeUser**</dt> <dt>&H03000000</dt> </dl>                                     | Message de demande utilisateur, \[ 1 \] est le numéro de message dans la [table d’erreurs](error-table.md).<br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt> </dl>                                         | Message d’information pour le journal, à ne pas afficher.<br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt> </dl>                 | Liste des fichiers en cours d’utilisation qui doivent être remplacés.<br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt> </dl>     | Demandez à déterminer un emplacement source valide.<br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt> </dl> | Message d’espace disque insuffisant.<br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt> </dl>             | Début de l’action, \[ 1 \] nom d’action, \[ 2 \] Description, \[ 3 \] modèle pour les messages ACTIONDATA.<br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt> </dl>                 | Données d’action. Les champs d’enregistrement correspondent au modèle de message ACTIONSTART.<br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt> </dl>                         | Informations sur la barre de progression. Consultez la description des champs d’enregistrement ci-dessous.<br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <dt> **msiMessageTypeCommonData**</dt> <dt>&H0B000000</dt> </dl>             | Pour activer le bouton Annuler défini \[ \] entre 1 et 2 \[ \] à 1. <br/> Pour désactiver le bouton Annuler défini \[ \] entre 1 et 2 et \[ 2 \] à 0<br/> |



 

</dd> <dt>

*enregistrement* 
</dt> <dd>

Objet [**Record**](record-object.md) requis contenant un champ spécifique au message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée



| Constante                                                                                              | Valeur         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <dt>**msiMessageStatusError**</dt> </dl>  | -1<br/> |
| <dl> <dt>**msiMessageStatusNone**</dt> </dl>   | 0<br/>  |
| <dl> <dt>**msiMessageStatusOk**</dt> </dl>     | 1<br/>  |
| <dl> <dt>**msiMessageStatusCancel**</dt> </dl> | 2<br/>  |
| <dl> <dt>**msiMessageStatusAbort**</dt> </dl>  | 3<br/>  |
| <dl> <dt>**msiMessageStatusRetry**</dt> </dl>  | 4<br/>  |
| <dl> <dt>**msiMessageStatusIgnore**</dt> </dl> | 5<br/>  |
| <dl> <dt>**msiMessageStatusYes**</dt> </dl>    | 6<br/>  |
| <dl> <dt>**msiMessageStatusNo**</dt> </dl>     | 7<br/>  |



 

## <a name="remarks"></a>Notes

**Champs d’enregistrement de message**

La rubrique suivante décrit les définitions de champs d’enregistrement lorsque msiMessageTypeProgress est transmis comme type de message.

Le champ 1 spécifie le type de message de progression. La signification des autres champs dépend de la valeur de ce champ. Les valeurs possibles qui peuvent être définies dans le champ 1 sont les suivantes.



| Nom du message     | Valeur | Description du champ 1                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| MasterReset      | 0     | Réinitialise la barre de progression et définit le nombre total de graduations attendu dans la barre.                                         |
| ActionInfo       | 1     | Fournit des informations relatives aux messages de progression qui doivent être envoyés par l’action en cours.                                 |
| ProgressReport   | 2     | Incrémente la barre de progression.                                                                                        |
| ProgressAddition | 3     | Permet à une action (telle que CustomAction) d’ajouter des graduations au nombre total attendu de la progression de la barre de progression. |



 

La signification du champ 2 dépend de la valeur du champ 1 comme suit.



| Valeur champ 1 | Description du champ 2                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| 0             | Nombre total de graduations attendu dans la barre de progression.                                                        |
| 1             | Nombre de graduations que la barre de progression déplace pour chaque message ActionData. Ce champ est ignoré si le champ 3 est égal à 0. |
| 2             | Nombre de graduations de la barre de progression.                                                                |
| 3             | Nombre de graduations à ajouter à la progression attendue totale.                                                         |



 

La signification du champ 3 dépend de la valeur du champ 1 comme suit.



| Valeur champ 1 | Valeur champ 3 | Description du champ 3                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| 0             | 0             | Barre de progression vers l’avant (de gauche à droite)                                                                            |
|               | 1             | Barre de progression vers l’arrière (de droite à gauche)                                                                           |
| 1             | 0             | L’action en cours enverra des messages ProgressReport explicites.                                                  |
|               | 1             | Incrémente la barre de progression du nombre de graduations spécifié dans le champ 2 chaque fois qu’un message ActionData est envoyé. |
| 2             | Inutilisé        |                                                                                                                 |
| 3             | Inutilisé        |                                                                                                                 |



 

La signification du champ 4 dépend de la valeur du champ 1 comme suit.



| Valeur champ 1 | Valeur champ 4 | Description du champ 4                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | 0             | L’exécution est en cours. Dans ce cas, l’interface utilisateur peut calculer et afficher le temps restant.                                                      |
|               | 1             | Création du script d’exécution. Dans ce cas, l’interface utilisateur peut afficher un message pour patienter pendant que le programme d’installation a terminé la préparation de l’installation. |
| 1             | Inutilisé        |                                                                                                                                                     |
| 2             | Inutilisé        |                                                                                                                                                     |
| 3             | Inutilisé        |                                                                                                                                                     |



 

**Affichage des boîtes de message**

Pour afficher une boîte de message avec des boutons et des icônes de type push, calculez la valeur de *genre* en ajoutant les styles de zone de message standard utilisés par **MessageBox** et **MessageBoxEx** à **msiMessageTypeError**, **msiMessageTypeWarning** ou **msiTypeUser**. Les options de bouton de commande disponibles pour VBScript sont vbOKOnly (Mo \_ OK), vbOKCancel (MB \_ OKCANCEL), VBABORTRETRYIGNORE (Mo \_ ABORTRETRYIGNORE), vbYesNoCancel (Mo \_ YESNOCANCEL), vbYesNo (Mo \_ YesNo) et vbRetryCancel (Mo \_ RETRYCANCEL). Les options d’icône disponibles pour VBScript sont vbCritical (Mo \_ ICONERROR), vbQuestion (MB \_ ICONQUESTION), VBEXCLAMATION (Mo \_ ICONWARNING) et vbInformation (Mo \_ ICONINFORMATION).

Par exemple, l’appel suivant envoie un message **msiMessageTypeError** avec l’icône vbExclamation et les boutons vbYesNo.


```VB
Session.Message &H01000034, record
```



Si une action personnalisée appelle la méthode de **message** , l’action personnalisée doit être en mesure de gérer une annulation par l’utilisateur et de retourner **msiDoActionStatusUserExit**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 
