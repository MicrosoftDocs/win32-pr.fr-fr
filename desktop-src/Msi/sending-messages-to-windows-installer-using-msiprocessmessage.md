---
description: Les messages envoyés à l’aide de MsiProcessMessage sont les mêmes que ceux reçus par la \_ fonction de rappel du gestionnaire INSTALLUI si MsiSetExternalUI a été appelé.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: envoyer des Messages à Windows Installer à l’aide de MsiProcessMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230052"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a>envoi de Messages à Windows Installer à l’aide de MsiProcessMessage

Les messages envoyés à l’aide de [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) sont les mêmes que ceux reçus par la fonction de rappel du [**\_ Gestionnaire INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera) si [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) a été appelé. dans le cas contraire, Windows Installer gère les messages. pour plus d’informations, consultez [analyse des Messages de Windows Installer](parsing-windows-installer-messages.md).

Par exemple, pour envoyer un \_ message d’erreur INSTALLMESSAGE avec l' \_ icône Mo ICONWARNING et les \_ boutons MB ABORTRETRYCANCEL :


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



Où *hInstall* est le descripteur de l’installation, fourni à une action personnalisée ou au descripteur *hProduct* à partir de [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) ou [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), et *hRec* est l’enregistrement contenant les informations d’erreur à mettre en forme. Pour plus d’informations sur la façon dont la mise en forme est effectuée, consultez [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).

Par défaut, si une \_ erreur INSTALLMESSAGE ou un \_ message INSTALLMESSAGE FATALEXIT est envoyé sans spécifier le type de bouton ou les types d’icône, MB \_ OK, aucune icône et Mo \_ DEFBUTTON1 sont utilisés.

Windows Le programme d’installation n’étiquette pas le bouton **abandonner** avec la chaîne « Abort » lors de l’affichage d’une MessageBox avec la \_ spécification du bouton ABORTRETRYIGNORE Mo, mais il étiquette le bouton avec la chaîne « Cancel ». Tous les messages d’erreur s’abstiennent d’utiliser le mot « Abort » et utilisent plutôt le mot « Cancel ».

Le paramètre *hRecord* de la fonction [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) dépend du type de message envoyé au [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). La liste suivante détaille les spécifications de l’enregistrement par rapport au type de message :

INSTALLMESSAGE \_ FATALEXIT

 

\_informations INSTALLMESSAGE

 

INSTALLMESSAGE \_ OUTOFDISKSPACE



| Champ         | Description                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | Modèle pour la mise en forme de la chaîne résultante. Pour plus d’informations, consultez [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) . Les champs de l’enregistrement sont référencés à l’aide \[ \] de 1 pour le champ 1, \[ 2 pour le \] champ 2, etc. |
| 1 à *n* | Tous les champs suivants sont directement liés aux champs référencés par le modèle dans le champ 0.                                                                                                                    |



 

Si le champ 0 a la valeur null, la chaîne reçue par le gestionnaire d’interface utilisateur est mise en forme comme suit : 1 : \[ données du champ 1 \] 2 : les \[ données du champ 2 \] signifient que, pour chaque champ de l’enregistrement, la chaîne contient le numéro de champ suivi des données stockées dans le champ.

Les messages d’information de [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) sont journalisés lorsque [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), l' [option de ligne de commande](command-line-options.md)« /l » ou la [stratégie de journalisation](logging.md) spécifient « I » ou INSTALLLOGMODE \_ info.

\_erreur INSTALLMESSAGE

 

\_Avertissement INSTALLMESSAGE

 

\_utilisateur INSTALLMESSAGE

Pour utiliser un message de la table d’erreurs.



| Champ         | Description                                           |
|---------------|-------------------------------------------------------|
| 0             | Doit avoir la valeur null.                                         |
| 1             | Numéro de message dans la [table d’erreurs](error-table.md). |
| 2 à *n* | Lié au message spécifié dans la table d’erreurs.  |



 

Par exemple,



| Champ | Type   | Données       |
|-------|--------|------------|
| 0     | string | null       |
| 1     | int    | 1304       |
| 2     | string | Myfile.txt |



 

Le message obtenu à partir du gestionnaire d’interface utilisateur est le suivant :

Erreur 1304. Erreur lors de l’écriture dans le fichier : Myfile.txt. Vérifiez que vous avez accès à ce répertoire.

Si le champ 0 n’est pas null, le message de la table d’erreurs est substitué. Au lieu de cela, le modèle de champ 0 détermine le format du message.

Le message peut également spécifier les boutons, y compris le bouton par défaut, et l’icône à utiliser avec le message comme indiqué ci-dessus. Les types de bouton et d’icône sont répertoriés dans le [**\_ Gestionnaire INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera).

INSTALLMESSAGE \_ COMMONDATA

Ce message est envoyé pour activer ou désactiver le bouton **Annuler** dans une boîte de dialogue de progression.



| Champ | Description                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Inutilisé.                                                                                                                                      |
| 1     | 2 fait référence au bouton **Annuler** .                                                                                                           |
| 2     | La valeur 1 indique que le bouton **Annuler** doit être visible. La valeur 0 indique que le bouton **Annuler** doit être invisible.<br/> |



 

Par exemple, pour désactiver ou masquer le bouton **Annuler** , l’enregistrement s’affiche comme suit.



| Champ | Type   | Données |
|-------|--------|------|
| 0     | string | null |
| 1     | int    | 2    |
| 2     | int    | 0    |



 

INSTALLMESSAGE \_ ACTIONSTART

 

INSTALLMESSAGE \_ ACTIONDATA

L' \_ enregistrement INSTALLMESSAGE ACTIONSTART détermine le format de l’enregistrement ActionData.



| Champ | Description                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| 0     | null                                                                                                          |
| 1     | Nom de l’action. Le nom de ce champ doit être non null.                                                         |
| 2     | Description de l’action.                                                                                           |
| 3     | Modèle d’action. Cette valeur est utilisée pour le ActionData dont le message est mis en forme en fonction de ce modèle. |



 

Ne faites pas référence au champ 0 dans le message de modèle d’action.

L' \_ enregistrement INSTALLMESSAGE ACTIONDATA est mis en forme comme suit.



| Champ         | Description                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | null                                                                                                                                               |
| 1 à *n* | Dépend du champ 3 du \_ message ou du modèle INSTALLMESSAGE ACTIONSTART correspondant spécifié dans la [table ActionText](actiontext-table.md). |



 

Par exemple, l' \_ enregistrement INSTALLMESSAGE ACTIONSTART.



| Champ | Type   | Données                                                            |
|-------|--------|-----------------------------------------------------------------|
| 0     | string | null                                                            |
| 1     | string | MyAction                                                        |
| 2     | string | Il s’agit de la description de « MyAction »                           |
| 3     | string | Modèle MyAction : les données champ1 sont \[ 1 \] . les données du champ 2 sont \[ 2 \] . |



 

Le modèle pour INSTALLMESSAGE \_ ACTIONSTART (Field 3) fait référence aux champs 1 et 2, l' \_ enregistrement INSTALLMESSAGE ACTIONDATA doit avoir 2 champs contenant les données justifiées. Les champs peuvent être des champs de type chaîne ou entier.

\_Enregistrement INSTALLMESSAGE ACTIONDATA.



| Champ | Type   | Données                    |
|-------|--------|-------------------------|
| 0     | string | null                    |
| 1     | int    | 2                       |
| 2     | string | ActionData pour MyAction |



 

INSTALLMESSAGE \_ FILESINUSE

L’enregistrement FILESINUSE est un enregistrement de longueur variable.



| Champ | Description                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Ce champ peut avoir la valeur null. Pour une installation à l’aide d’une interface utilisateur de base, ce champ peut spécifier un texte statique à afficher dans le [contrôle ListBox](listbox-control.md) de la [boîte de dialogue FilesInUse](filesinuse-dialog.md). Pour une installation à l’aide d’une interface utilisateur complète, ce champ n’a aucun effet, car le texte est spécifié par la création de la boîte de dialogue FilesInUse personnalisée. |
| 1     | Nom du fichier en cours d’utilisation.                                                                                                                                                                                                                                                                                                                                        |
| 2     | Ce champ identifie le processus contenant le fichier en cours d’utilisation. **Windows Installer version 4,0 :** L’ID de processus (PID) du processus, ou le titre de la fenêtre pour le processus.<br/> **Windows Installer la version 3,1 et les versions antérieures :** Ce champ doit correspondre à l’ID de processus (PID) du processus.<br/>                                                      |



 

Par exemple, pour envoyer un message FilesInUse indiquant que deux fichiers sont en cours d’utilisation, red.exe et blue.exe, l’enregistrement contient quatre champs plus le champ 0. Le format de l’enregistrement est comme indiqué dans le tableau suivant. cet exemple requiert Windows Installer version 4,0.

**Windows Installer la version 3,1 et les versions antérieures :** Dans l’exemple suivant, les champs 2 et 4 doivent contenir les PID des processus contenant red.exe et blue.exe en cours d’utilisation.



| Champ | Description       |
|-------|-------------------|
| 0     | null              |
| 1     | Red.exe           |
| 2     | Titre de la fenêtre rouge  |
| 3     | Blue.exe          |
| 4     | Titre de fenêtre bleue |



 

> [!Note]  
> sur Windows Installer version 4,0, si le PID passé à partir du service n’a pas de titre de fenêtre, tel qu’une application de barre d’état système, le fichier ne s’affiche pas et le journal détaillé contient les messages suivants.

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

INSTALLMESSAGE \_ RESOLVESOURCE

L' \_ enregistrement INSTALLMESSAGE RESOLVESOURCE contient sept champs. Pour \_ que INSTALLMESSAGE RESOLVESOURCE fonctionne correctement, un gestionnaire d’interface utilisateur externe peut ne pas gérer le \_ message INSTALLMESSAGE RESOLVESOURCE. Windows Le programme d’installation doit gérer le \_ message INSTALLMESSAGE RESOLVESOURCE. Autrement dit, le gestionnaire d’interface utilisateur externe retourne 0 pour indiquer « aucune action effectuée » lors du filtrage du \_ message INSTALLMESSAGE RESOLVESOURCE. La meilleure pratique consiste à éviter d’envoyer un message RESOLVESOURCE.



| Champ | Description                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | null                                                                                                                                                               |
| 1     | null                                                                                                                                                               |
| 2     | Nom du package.                                                                                                                                                      |
| 3     | Code du produit.                                                                                                                                                      |
| 4     | Chemin d’accès relatif, s’il est connu, peut avoir la valeur null.                                                                                                                               |
| 5     | 0                                                                                                                                                                  |
| 6     | Indique s’il faut valider le code du package. La valeur « 1 » indique que le code du package doit être validé. La valeur « 0 » indique que le package ne doit pas être validé. |
| 7     | Disque requis à partir de la table de supports. La valeur « 0 » indique que tous les disques sont acceptables.                                                                              |



 

 

 




