---
title: Boîtes de dialogue Ouvrir et enregistrer sous
description: La boîte de dialogue Ouvrir permet à l’utilisateur de spécifier le lecteur, le répertoire et le nom d’un fichier ou d’un ensemble de fichiers à ouvrir.
ms.assetid: 5676ca9d-daca-40bf-8881-def2ff841c58
keywords:
- Bibliothèque de boîtes de dialogue communes
- boîtes de dialogue communes
- Boîte de dialogue Ouvrir
- Enregistrer sous, boîte de dialogue
- personnalisation de la boîte de dialogue Ouvrir
- personnalisation de la boîte de dialogue Enregistrer sous
- boîtes de dialogue, ouvrir
- boîtes de dialogue, enregistrer sous
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 605040af3aafe9d7739ebd069a7c0607402940c8
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590826"
---
# <a name="open-and-save-as-dialog-boxes"></a>Boîtes de dialogue Ouvrir et enregistrer sous

> [!NOTE]
> La fonction [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) est illustrée dans l' [exemple fichier en cours d’utilisation](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse).

\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/windows/win32/shell/common-file-dialog). Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]

La boîte de dialogue **ouvrir** permet à l’utilisateur de spécifier le lecteur, le répertoire et le nom d’un fichier ou d’un ensemble de fichiers à ouvrir. Vous créez et affichez une boîte de dialogue **ouvrir** en initialisant une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) et en passant la structure à la fonction [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) .

La boîte de dialogue **Enregistrer sous** permet à l’utilisateur de spécifier le lecteur, le répertoire et le nom d’un fichier à enregistrer. Vous créez et affichez une boîte de dialogue **Enregistrer sous** en initialisant une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) et en passant la structure à la fonction [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) .

Les boîtes de dialogue **ouvrir** et **Enregistrer sous** de style Explorateur fournissent des fonctionnalités d’interface utilisateur similaires à celles de l’Explorateur Windows. Toutefois, le système continue à prendre en charge les anciennes boîtes de dialogue **ouvrir** et **Enregistrer sous** pour les applications qui doivent être cohérentes avec l’interface utilisateur de type ancien.

En plus de la différence de l’apparence, les boîtes de dialogue de style Explorateur et ancien diffèrent au niveau de leur utilisation des modèles personnalisés et des procédures de Hook pour la personnalisation des boîtes de dialogue. Toutefois, les boîtes de dialogue de style Explorateur et ancien ont le même comportement pour la plupart des opérations de base, telles que la spécification d’un filtre de nom de fichier, la validation de l’entrée de l’utilisateur et l’obtention du nom de fichier spécifié par l’utilisateur. Pour plus d’informations sur les boîtes de dialogue de style Explorateur et ancien, consultez [Personnalisation de la boîte de dialogue Ouvrir et enregistrer sous](#open-and-save-as-dialog-box-customization).

L’illustration suivante montre une boîte de dialogue d' **ouverture** de style Explorateur typique.

![ouvrir un fichier (boîte de dialogue)](images/opendialogboxxp.png)

L’illustration suivante montre une boîte de dialogue standard **Enregistrer sous** de type Explorateur.

![boîte de dialogue Enregistrer le fichier](images/saveasdialogboxxp.png)

Si l’utilisateur spécifie un nom de fichier et clique sur le bouton **OK** , [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) ou [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) retourne la **valeur true**. La mémoire tampon vers laquelle pointe le membre **lpstrFile** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) contient le chemin d’accès complet et le nom de fichier spécifiés par l’utilisateur.

Si l’utilisateur annule la boîte de dialogue **ouvrir** ou **Enregistrer sous** , ou qu’une erreur se produit, la fonction retourne **false**. Pour déterminer la cause de l’erreur, appelez la fonction [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) pour récupérer la valeur d’erreur étendue. Si la mémoire tampon **lpstrFile** est trop petite pour recevoir le nom complet, **CommDlgExtendedError** retourne **FNERR \_ BUFFERTOOSMALL** et les 2 premiers octets de la mémoire tampon vers laquelle pointe le membre **lpstrFile** sont définis sur une valeur entière spécifiant la taille requise pour recevoir le nom complet.

Les rubriques suivantes sont présentées dans cette section.

-   [Noms et répertoires de fichiers](#file-names-and-directories)
-   [Filtres](#filters)
-   [Validation de fichiers et de répertoires](#file-and-directory-validation)
-   [Personnalisation de la boîte de dialogue Ouvrir et enregistrer sous](#open-and-save-as-dialog-box-customization)
-   [Procédures de hook de style Explorer](#explorer-style-hook-procedures)
-   [Modèles personnalisés de style Explorateur](#explorer-style-custom-templates)
-   [Identificateurs de contrôle de style Explorateur](#explorer-style-control-identifiers)
-   [Personnalisation des boîtes de dialogue Old-Style](#customizing-old-style-dialog-boxes)

## <a name="file-names-and-directories"></a>Noms et répertoires de fichiers

Les informations contenues dans cette section s’appliquent aux boîtes de dialogue **ouvrir** et **Enregistrer sous** de style Explorateur et ancien style.

Avant d’appeler les fonctions [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) ou [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) , le membre **lpstrFile** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) doit pointer vers la mémoire tampon pour recevoir le nom de fichier. Le membre **nMaxFile** doit spécifier la taille, en caractères, de la mémoire tampon **lpstrFile** . Pour une fonction ANSI, il s’agit du nombre d’octets, mais pour une fonction Unicode, il s’agit du nombre de caractères.

Si l’utilisateur spécifie un nom de fichier et clique sur le bouton **OK** , la boîte de dialogue copie le lecteur, le répertoire et le nom de fichier sélectionnés dans la mémoire tampon **lpstrFile** . La fonction définit également les membres **nFileOffset** et **nFileExtension** sur les décalages, en caractères, entre le début de la mémoire tampon et le nom de fichier et l’extension de nom de fichier, respectivement.

Pour récupérer uniquement le nom de fichier et l’extension, définissez le membre **lpstrFileTitle** pour qu’il pointe vers une mémoire tampon et définissez le membre **nMaxFileTitle** sur la taille, en caractères, de la mémoire tampon. Vous pouvez également transmettre la mémoire tampon **lpstrFile** dans un appel à la fonction [**GetFileTitle**](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea) pour obtenir le nom complet du fichier sélectionné. Notez, toutefois, que le nom de fichier retourné par **GetFileTitle** comprend une extension uniquement s’il s’agit de la préférence de l’utilisateur pour l’affichage des noms de fichiers.

La boîte de dialogue utilise le répertoire actif pour le processus appelant comme répertoire initial à partir duquel les fichiers et les répertoires sont affichés. Utilisez les fonctions [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) et [**SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) pour obtenir et modifier le répertoire actif d’un processus. Pour spécifier un autre répertoire initial sans modifier votre répertoire actif, utilisez le membre **lpstrInitialDir** pour spécifier le nom d’un répertoire. La boîte de dialogue change automatiquement votre répertoire actuel lorsque l’utilisateur sélectionne un autre lecteur ou répertoire. Pour empêcher la boîte de dialogue de changer votre répertoire actif, définissez l’indicateur **OFN \_ NOCHANGEDIR** . Cet indicateur n’empêche pas l’utilisateur de changer de répertoire pour rechercher un fichier.

Pour spécifier une extension de nom de fichier par défaut, utilisez le membre **lpstrDefExt** . Si l’utilisateur spécifie un nom de fichier qui n’a pas d’extension, la boîte de dialogue ajoute votre extension par défaut. Si vous spécifiez une extension par défaut et que l’utilisateur spécifie un nom de fichier avec une extension différente, la boîte de dialogue définit l’indicateur **OFN \_ EXTENSIONDIFFERENT** .

Pour permettre à l’utilisateur de sélectionner plusieurs fichiers dans un répertoire, définissez l’indicateur **OFN \_ ALLOWMULTISELECT** . Pour la compatibilité avec les anciennes applications, la boîte de dialogue sélection multiple par défaut utilise l’ancienne interface utilisateur. Pour afficher une boîte de dialogue de sélection multiple de type Explorateur, vous devez également définir l’indicateur **OFN \_ Explorer** .

Si l’utilisateur sélectionne plusieurs fichiers, la mémoire tampon vers laquelle pointe le membre **lpstrFile** retourne le chemin d’accès au répertoire actif, suivi des noms de fichiers des fichiers sélectionnés. Le membre **nFileOffset** est le décalage par rapport au premier nom de fichier, et le membre **nFileExtension** n’est pas utilisé. Le tableau suivant décrit la différence entre les boîtes de dialogue de style Explorateur et de style ancien dans le retour de plusieurs noms de fichiers.



| Style de boîte de dialogue            | Description                                                                                                                                                                                                               |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boîtes de dialogue de style Explorateur | Les chaînes de nom de fichier et de répertoire sont séparées par des **valeurs NULL** , avec un caractère **null** supplémentaire après le dernier nom de fichier. Ce format permet aux boîtes de dialogue de style Explorateur de retourner des noms de fichiers longs qui incluent des espaces. |
| Anciennes boîtes de dialogue      | Les chaînes de noms de répertoires et de fichiers sont séparées par des espaces. Pour les noms de fichiers avec des espaces, la fonction utilise des noms de fichiers courts.                                                                                              |



 

Vous pouvez utiliser la fonction [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) pour effectuer une conversion entre des noms de fichiers longs et courts.

Si vous spécifiez **OFN \_ ALLOWMULTISELECT** et que l’utilisateur sélectionne un seul fichier, la chaîne **lpstrFile** n’a pas de séparateur entre le chemin d’accès et le nom de fichier.

## <a name="filters"></a>Filtres

Les informations contenues dans cette section s’appliquent à la fois aux boîtes de dialogue **ouvrir** et **Enregistrer sous** d’un style d’explorateur.

Vous pouvez fournir des filtres de nom de fichier pour aider l’utilisateur à limiter les noms de fichiers que la boîte de dialogue affiche. Un filtre de nom de fichier se compose d’une paire de chaînes se terminant par un caractère null, d’une description et d’un modèle, d’une concaténation à l’autre. La boîte de dialogue affiche la description pour permettre à l’utilisateur de choisir le filtre à utiliser. et utilise le modèle pour sélectionner les fichiers à afficher.

Pour spécifier les filtres, définissez le membre **lpstrFilter** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) de façon à ce qu’il pointe vers une mémoire tampon qui contient un tableau de paires de chaînes de filtre. La dernière chaîne dans le tableau doit être suivie d’un caractère null supplémentaire.

Une chaîne de modèle peut être une combinaison de caractères de nom de fichier valides et de l’astérisque ( \* ). L’astérisque est un caractère générique qui représente toute combinaison de caractères de nom de fichier valides. La boîte de dialogue affiche uniquement les fichiers qui correspondent au modèle. Pour spécifier plusieurs modèles pour la même description, vous devez utiliser un point-virgule (;) pour séparer les modèles. Notez que les espaces dans la chaîne de modèle peuvent produire des résultats inattendus.

Le fragment de code suivant spécifie deux filtres. Le filtre avec la description « source » a deux modèles. Si l’utilisateur sélectionne ce filtre, la boîte de dialogue affiche uniquement les fichiers qui ont le. C et. Extensions CXX. Notez que, dans le langage de programmation C, une chaîne placée entre guillemets doubles est terminée par un caractère null.


```
OPENFILENAME ofn;       // common dialog box structure

ofn.lpstrFilter = "Source\0*.C;*.CXX\0All\0*.*\0"
ofn.nFilterIndex = 1;
```



Le membre **nFilterIndex** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) spécifie un index qui indique le filtre utilisé initialement par la boîte de dialogue. Le premier filtre de la mémoire tampon a l’index 1, le deuxième 2, et ainsi de suite. Si l’utilisateur modifie le filtre lors de l’utilisation de la boîte de dialogue, le membre **nFilterIndex** est défini sur l’index du filtre sélectionné lors du retour.

Vous pouvez créer un filtre personnalisé en définissant le membre **lpstrCustomFilter** sur l’adresse d’une mémoire tampon qui contient un filtre unique et en définissant le membre **nMaxCustFilter** sur la taille de la mémoire tampon, en caractères ou en octets. La boîte de dialogue place toujours le filtre personnalisé au début de la liste de filtres et, au retour, met toujours à jour la partie de modèle du filtre avec le modèle du filtre sélectionné par l’utilisateur.

Pour les boîtes de dialogue de style Explorateur, l’extension par défaut peut changer si l’utilisateur sélectionne un filtre différent. Si l’utilisateur sélectionne un filtre dont le premier modèle se présente sous la forme \* .*xxx* (autrement dit, l’extension n’inclut pas de caractère générique), la boîte de dialogue utilise *xxx* comme extension par défaut. Cela se produit uniquement si vous avez spécifié une extension par défaut dans le membre **lpstrDefExt** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . Par exemple, si l’utilisateur sélectionne la «source \\ 0 \* . C ; \* . CXX \\ 0», l’extension par défaut devient « C ». Toutefois, si vous aviez défini le filtre sur «source \\ 0 \* . C \* \\ 0», l’extension par défaut ne change pas, car l’extension contient un caractère générique.

Le message de notification [**CDN \_ INCLUDEITEM**](cdn-includeitem.md) fournit une autre méthode pour filtrer les noms que la boîte de dialogue affiche. Pour utiliser ce message, fournissez une procédure de hook [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) et spécifiez l’indicateur **OFN \_ ENABLEINCLUDENOTIFY** dans la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) lorsque vous créez la boîte de dialogue. Chaque fois que l’utilisateur ouvre un dossier, la boîte de dialogue envoie une notification **\_ INCLUDEITEM CDN** à votre procédure de Hook pour chaque élément dans le dossier qui vient d’être ouvert. La valeur de retour de la procédure de raccordement indique si la boîte de dialogue doit afficher l’élément dans la liste d’éléments du dossier.

## <a name="file-and-directory-validation"></a>Validation de fichiers et de répertoires

Sauf indication contraire, les informations contenues dans cette section s’appliquent aux boîtes de dialogue **ouvrir** et **Enregistrer sous** de style Explorateur et ancien style.

La boîte de dialogue valide automatiquement les noms de fichiers tapés par l’utilisateur pour s’assurer que les noms contiennent uniquement des caractères valides. Pour remplacer la validation de caractère de nom de fichier, définissez l’indicateur **\_ novalidate OFN** .

Pour forcer la boîte de dialogue à vérifier que l’utilisateur a spécifié le nom d’un fichier existant, définissez l’indicateur **OFN \_ FILEMUSTEXIST** . Pour forcer la vérification que le chemin d’accès spécifié existe, définissez l’indicateur **OFN \_ PATHMUSTEXIST** . Si vous définissez l’indicateur **OFN \_ CREATEPROMPT** , la boîte de dialogue demande à l’utilisateur l’autorisation de créer un fichier inexistant. Si cet indicateur est défini et que l’utilisateur choisit de créer un nouveau fichier, la boîte de dialogue se ferme et la fonction retourne le nom spécifié. Dans le cas contraire, la boîte de dialogue reste ouverte.

Lorsque vous utilisez la boîte de dialogue **Enregistrer sous** , vous pouvez indiquer à la boîte de dialogue de demander à l’utilisateur l’autorisation de remplacer un fichier existant en définissant l’indicateur **OFN \_ OVERWRITEPROMPT** .

Par défaut, la boîte de dialogue crée un fichier de test de longueur zéro pour déterminer si un nouveau fichier peut être créé dans le répertoire sélectionné. Pour empêcher la création de ce fichier de test, définissez l’indicateur **OFN \_ NOTESTFILECREATE** .

Si vous activez une procédure de Hook, la boîte de dialogue notifie votre procédure de raccordement lorsqu’une violation de partage réseau se produit pour le nom de fichier spécifié par l’utilisateur. Si vous définissez l’indicateur **OFN \_ Explorer** , la boîte de dialogue envoie le message [**CDN \_ SHAREVIOLATION**](cdn-shareviolation.md) à la procédure de Hook. Si vous ne définissez pas **OFN \_ Explorer**, la boîte de dialogue envoie le message [**SHAREVISTRING**](sharevistring.md) Registered à la procédure de Hook. Pour empêcher la boîte de dialogue d’envoyer des notifications pour les violations de partage, définissez l’indicateur **OFN \_ SHAREAWARE** .

Si l’utilisateur sélectionne la case à cocher en lecture seule, la boîte de dialogue définit l’indicateur **\_ ReadOnly OFN** lors du retour. Pour masquer la case à cocher **ouvrir en lecture seule** , définissez l’indicateur **OFN \_ HIDEREADONLY** . Pour empêcher la boîte de dialogue de retourner les noms des fichiers existants qui ont l’attribut de lecture seule, définissez l’indicateur **OFN \_ NOREADONLYRETURN** .

Pour empêcher la boîte de dialogue de déréférencer les fichiers de liaison, définissez la valeur **\_ NODEREFERENCELINKS OFN** . Dans ce cas, la boîte de dialogue retourne le nom du fichier de liaison au lieu du nom du fichier référencé par le fichier de liaison.

## <a name="open-and-save-as-dialog-box-customization"></a>Personnalisation de la boîte de dialogue Ouvrir et enregistrer sous

Vous pouvez personnaliser une boîte de dialogue **ouvrir** ou **Enregistrer sous** en fournissant une procédure de raccordement, un modèle personnalisé, ou les deux. Toutefois, les versions de type Explorateur et ancien style des boîtes de dialogue diffèrent au niveau de leur utilisation des modèles personnalisés et des procédures de Hook.

Pour plus d’informations sur la personnalisation d’une boîte de dialogue de style Explorateur, consultez [procédures de hook de style](#explorer-style-hook-procedures)Explorateur, [modèles personnalisés de style Explorateur](#explorer-style-custom-templates)et [identificateurs de contrôle de style Explorateur](#explorer-style-control-identifiers). Pour plus d’informations sur la personnalisation d’une ancienne boîte de dialogue de style, consultez [Personnalisation des boîtes de dialogue de Old-Style](#customizing-old-style-dialog-boxes).

Le tableau suivant résume les différences entre les deux styles.



| Personnalisation                  | Description                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Procédure de hook de style Explorer  | La procédure de hook reçoit des messages de notification envoyés à partir de la boîte de dialogue commune et des messages pour tous les contrôles supplémentaires que vous avez définis en spécifiant un modèle de boîte de dialogue enfant. La procédure de hook ne reçoit pas de messages pour les contrôles standard de la boîte de dialogue par défaut. |
| Modèle personnalisé de style Explorateur | Le système utilise le modèle personnalisé pour créer une boîte de dialogue enfant. Le modèle peut définir des contrôles supplémentaires et peut spécifier l’emplacement du cluster de contrôles standard. Le modèle personnalisé ne remplace pas le modèle par défaut.                                          |
| Procédure de hook de style ancien       | La procédure de hook reçoit tous les messages envoyés à la boîte de dialogue, y compris les messages pour les contrôles standard et les contrôles personnalisés. La procédure de hook reçoit également les messages enregistrés à partir de la boîte de dialogue commune.                                                         |
| Ancien modèle personnalisé      | Le modèle personnalisé remplace le modèle par défaut. Créez le modèle personnalisé en modifiant le modèle par défaut spécifié dans le fichier FileOpen. dlg.                                                                                                                                  |



 

Le titre par défaut pour les deux boîtes de dialogue de style Explorateur et ancien est soit «**ouvrir**», soit «**Enregistrer sous**». Pour modifier le titre, spécifiez le nouveau titre dans le membre **lpstrTitle** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .

La ruche de Registre **HKEY \_ Current \_ User** d’un utilisateur peut contenir des valeurs qui personnalisent le contenu des boîtes de dialogue **ouvrir** et **Enregistrer sous** de style Explorateur. Ces entrées de Registre affectent uniquement les boîtes de dialogue affichées pour l’utilisateur associé à la ruche du Registre.

Pour masquer les fonctionnalités des boîtes de dialogue **ouvrir** et **Enregistrer sous** d’un navigateur, un administrateur peut définir les valeurs du tableau suivant sous cette sous-clé :

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
```



| Nom de la valeur       | Valeur | Signification                                  |
|------------------|-------|------------------------------------------|
| **NoPlacesBar**  | 1     | Masque la barre des emplacements.                    |
| **NoFileMRU**    | 1     | Masque la liste des derniers fichiers utilisés (MRU). |
| **NoBackButton** | 1     | Masque le bouton **précédent** .               |



 

Le contenu de la barre **emplacements** est déterminé par le contenu de la sous-clé suivante :

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
                     Placesbar
```

Actuellement, il ne peut y avoir que cinq entrées sous cette clé, et l’index de valeur/nom est de base zéro. Les noms des entrées doivent être Place0, place1, place2, place3 et Place4. Les valeurs des entrées peuvent être **reg \_ DWORD**, **reg \_ SZ** ou **reg Expand valeurs \_ \_ SZ** qui identifient les emplacements à inclure dans la barre des emplacements.



| Type de valeur                         | Signification                                                                                                   |
|------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **\_valeur DWORD reg**                     | Valeur CSIDL qui identifie un dossier. Pour obtenir la liste des valeurs CSIDL, consultez [**valeurs CSIDL**](../shell/csidl.md). |
| **Reg \_ SZ** ou **reg \_ développé \_ SZ** | Chaîne terminée par le caractère null qui spécifie un chemin d’accès valide.                                                     |



 

## <a name="explorer-style-hook-procedures"></a>Procédures de hook Explorer-Style

Vous pouvez personnaliser une boîte de dialogue **ouvrir** ou **Enregistrer sous** d’un navigateur en fournissant une procédure de raccordement, un modèle personnalisé, ou les deux. Si vous fournissez une procédure de raccordement pour une boîte de dialogue de style Explorateur, le système crée une boîte de dialogue qui est un enfant de la boîte de dialogue par défaut. La procédure de raccordement agit comme procédure de dialogue pour la boîte de dialogue enfant. Cette boîte de dialogue enfant est basée sur le modèle personnalisé ou sur un modèle par défaut si aucun n’est fourni. Pour plus d’informations, consultez [modèles personnalisés de style Explorateur](#explorer-style-custom-templates).

Pour activer une procédure de Hook pour une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur, utilisez la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) lorsque vous créez la boîte de dialogue. Définissez les **indicateurs OFN \_ ENABLEHOOK** et **OFN \_ Explorer** dans le membre **Flags** et spécifiez l’adresse d’une procédure de hook [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) dans le membre **lpfnHook** . Si vous fournissez une procédure de raccordement et omettez l’indicateur **OFN \_ Explorer** , vous devez utiliser une procédure de hook [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) . vous obtiendrez alors l’interface utilisateur de type ancien. Pour plus d’informations, consultez [Personnalisation des boîtes de dialogue de Old-Style](#customizing-old-style-dialog-boxes).

Une procédure de raccordement de type Explorateur reçoit un grand nombre de messages lorsque la boîte de dialogue est ouverte. Ces options en question sont les suivantes :

-   Le message [**WM \_ INITDIALOG**](wm-initdialog.md) et d’autres messages de boîte de dialogue standard tels que le message de couleur de contrôle [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) .
-   Ensemble de messages de notification [**WM \_ Notify**](../controls/wm-notify.md) indiquant les actions effectuées par l’utilisateur ou d’autres événements de la boîte de dialogue.
-   Messages pour tous les contrôles supplémentaires que vous avez définis en spécifiant un modèle de boîte de dialogue enfant.

En outre, il existe un ensemble de messages que vous pouvez envoyer à une boîte de dialogue de type Explorateur pour obtenir des informations ou contrôler le comportement et l’apparence de la boîte de dialogue.

Si vous fournissez une procédure de raccordement pour une boîte de dialogue de style Explorateur, la procédure de boîte de dialogue par défaut crée une boîte de dialogue enfant lorsque la procédure de boîte de dialogue par défaut traite son message [**WM \_ INITDIALOG**](wm-initdialog.md) . La procédure de raccordement agit comme procédure de dialogue pour la boîte de dialogue enfant. À ce stade, la procédure de hook reçoit son propre message **WM \_ INITDIALOG** avec le paramètre *lParam* défini sur l’adresse de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) utilisée pour initialiser la boîte de dialogue. Une fois que la boîte de dialogue enfant a fini de traiter son propre message **WM \_ INITDIALOG** , la procédure de dialogue par défaut déplace les contrôles standard, si nécessaire, pour faire de la place pour tous les contrôles supplémentaires de la boîte de dialogue enfant. La procédure de dialogue par défaut envoie ensuite le message de notification [**CDN \_ INITDONE**](cdn-initdone.md) à la procédure de Hook.

La procédure de hook reçoit des messages de notification de notification [**WM \_**](../controls/wm-notify.md) indiquant les actions effectuées par l’utilisateur dans la boîte de dialogue. Vous pouvez utiliser certains de ces messages pour contrôler le comportement de la boîte de dialogue. Par exemple, la procédure de raccordement reçoit le message [**CDN \_ FILEOK**](cdn-fileok.md) lorsque l’utilisateur choisit un nom de fichier et clique sur le bouton **OK** . En réponse à ce message, la procédure de hook peut utiliser la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) pour rejeter le nom sélectionné et forcer la boîte de dialogue à rester ouverte.

Le paramètre *lParam* pour chaque message [**WM \_ Notify**](../controls/wm-notify.md) est un pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) ou [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) qui définit l’action. Le membre de **code** dans l’en-tête de cette structure contient l’un des messages de notification suivants.



| Message                                           | Signification                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_FILEOK CDN**](cdn-fileok.md)                 | L’utilisateur a cliqué sur le bouton **OK** . la boîte de dialogue va être fermée.                                                                                                                                                                                                                          |
| [**\_FOLDERCHANGE CDN**](cdn-folderchange.md)     | L’utilisateur a ouvert un nouveau dossier ou répertoire.                                                                                                                                                                                                                                                     |
| [**\_aide CDN**](cdn-help.md)                     | L’utilisateur a cliqué sur le bouton **aide** .                                                                                                                                                                                                                                                          |
| [**\_INCLUDEITEM CDN**](cdn-includeitem.md)       | Détermine si un élément doit être affiché. Lorsque l’utilisateur ouvre un nouveau dossier ou répertoire, le système envoie cette notification pour chaque élément du dossier ou du répertoire. Le système envoie cette notification uniquement si l’indicateur **OFN \_ ENABLEINCLUDENOTIFY** a été défini.                          |
| [**\_INITDONE CDN**](cdn-initdone.md)             | Le système a terminé l’initialisation de la boîte de dialogue et la boîte de dialogue a terminé le traitement du message [**WM \_ INITDIALOG**](wm-initdialog.md) . En outre, le système a terminé la disposition des contrôles dans la boîte de dialogue commune pour faire de la place pour les contrôles de la boîte de dialogue enfant (le cas échéant). |
| [**\_selChange CDN**](cdn-selchange.md)           | L’utilisateur a sélectionné un nouveau fichier ou dossier dans la liste des fichiers.                                                                                                                                                                                                                                     |
| [**\_SHAREVIOLATION CDN**](cdn-shareviolation.md) | La boîte de dialogue commune a rencontré une violation de partage sur le fichier sur le le le sujet du renvoi.                                                                                                                                                                                                        |
| [**\_TYPECHANGE CDN**](cdn-typechange.md)         | L’utilisateur a sélectionné un nouveau type de fichier dans la liste des types de fichiers.                                                                                                                                                                                                                                 |



 

Ces messages de [**\_ notification WM**](../controls/wm-notify.md) remplacent les messages inscrits [**FILEOKSTRING**](fileokstring.md), [**LBSELCHSTRING**](lbselchstring.md), [**SHAREVISTRING**](sharevistring.md)et [**HELPMSGSTRING**](helpmsgstring.md) utilisés par les versions précédentes des boîtes de dialogue **ouvrir** et **Enregistrer sous** . Toutefois, la procédure de hook reçoit également le message remplacé après le **message \_ WM Notify** si le traitement de **\_ notification WM** n’utilise pas [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) pour définir une valeur **\_ MSGRESULT DWL** différente de zéro.

Pour récupérer les informations relatives à l’état de la boîte de dialogue ou contrôler le comportement et l’apparence de la boîte de dialogue, la procédure de raccordement peut envoyer les messages suivants à la boîte de dialogue.



| Message                                             | Signification                                                                                                                                                                                                                  |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_GETFILEPATH CDM**](cdm-getfilepath.md)         | Récupère le chemin d’accès et le nom de fichier du fichier sélectionné.                                                                                                                                                                   |
| [**\_GETFOLDERIDLIST CDM**](cdm-getfolderidlist.md) | Récupère la liste d’identificateurs d’éléments correspondant au dossier actif ouvert par la boîte de dialogue. Pour plus d’informations sur les listes d’identificateurs d’éléments, consultez [Introduction à l’espace de noms Shell](/windows/desktop/shell/namespace-intro). |
| [**\_GETFOLDERPATH CDM**](cdm-getfolderpath.md)     | Récupère le chemin d’accès du dossier ou du répertoire actif pour la boîte de dialogue.                                                                                                                                                |
| [**\_GETSPEC CDM**](cdm-getspec.md)                 | Récupère le nom de fichier (sans le chemin d’accès) du fichier actuellement sélectionné dans la boîte de dialogue.                                                                                                                       |
| [**\_HIDECONTROL CDM**](cdm-hidecontrol.md)         | Masque le contrôle spécifié.                                                                                                                                                                                             |
| [**\_SETCONTROLTEXT CDM**](cdm-setcontroltext.md)   | Définit le texte dans le contrôle spécifié.                                                                                                                                                                                  |
| [**\_SETDEFEXT CDM**](cdm-setdefext.md)             | Définit l’extension de nom de fichier par défaut pour la boîte de dialogue.                                                                                                                                                                 |



 

## <a name="explorer-style-custom-templates"></a>Explorer-Style des modèles personnalisés

Pour définir des contrôles supplémentaires pour une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur, utilisez la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) pour spécifier un modèle pour une boîte de dialogue enfant qui contient les contrôles supplémentaires. Si votre modèle de boîte de dialogue enfant est une ressource d’une application ou d’une bibliothèque de liens dynamiques, définissez l’indicateur **OFN \_ ENABLETEMPLATE** dans le membre **Flags** et utilisez les membres **HINSTANCE** et **lpTemplateName** de la structure pour identifier le module et le nom de la ressource. Si le modèle est déjà en mémoire, définissez l’indicateur **OFN \_ ENABLETEMPLATEHANDLE** et utilisez le membre **HINSTANCE** pour identifier l’objet mémoire qui contient le modèle. Lorsque vous fournissez un modèle de boîte de dialogue enfant pour une boîte de dialogue de type Explorateur, vous devez également définir l’indicateur **OFN \_ Explorer** ; dans le cas contraire, le système suppose que vous fournissez un modèle de remplacement pour une boîte de dialogue de style ancien. En général, si vous fournissez des contrôles supplémentaires, vous devez également fournir une [procédure de hook de style Explorateur](#explorer-style-hook-procedures) pour traiter les messages des nouveaux contrôles.

Vous pouvez créer votre modèle de boîte de dialogue enfant de la même façon que vous le feriez pour tout autre modèle, sauf que vous devez spécifier les styles **WS \_ Child** et **WS \_ CLIPSIBLINGS** et spécifier les styles de **\_ contrôle** **DS \_ 3DLOOK** et DS. Le système requiert le style **WS \_ Child** , car votre modèle définit une boîte de dialogue enfant de la boîte de dialogue **ouvrir** ou **Enregistrer sous** par défaut. Le style **WS \_ CLIPSIBLINGS** garantit que la boîte de dialogue enfant ne dessine pas sur l’un des contrôles de la boîte de dialogue par défaut. Le style **DS \_ 3DLOOK** garantit que l’apparence des contrôles dans la boîte de dialogue enfant est cohérente avec les contrôles de la boîte de dialogue par défaut. Le style de **\_ contrôle du service d’annuaire** permet de s’assurer que l’utilisateur peut utiliser l’onglet et d’autres touches de navigation pour se déplacer entre tous les contrôles, par défaut ou personnalisés, dans la boîte de dialogue personnalisée.

Pour faire de la place pour les nouveaux contrôles, le système développe la boîte de dialogue par défaut en se sur la largeur et la hauteur de la boîte de dialogue personnalisée. Par défaut, tous les contrôles de la boîte de dialogue personnalisée sont positionnés sous les contrôles dans la boîte de dialogue par défaut. Toutefois, vous pouvez remplacer ce positionnement par défaut en incluant un contrôle de texte statique dans votre modèle de boîte de dialogue personnalisé et en lui assignant la valeur de l’identificateur de contrôle de **stc32**. (Cette valeur est définie dans le fichier d’en-tête Dlgs. h.) Dans ce cas, le système utilise le contrôle comme point de référence pour déterminer où positionner les nouveaux contrôles. Tous les nouveaux contrôles situés au-dessus et à gauche du contrôle **stc32** sont positionnés au même niveau et à gauche des contrôles dans la boîte de dialogue par défaut. Les nouveaux contrôles situés sous et à droite du contrôle **stc32** sont positionnés en dessous et à droite des contrôles par défaut. En général, chaque nouveau contrôle est positionné de façon à ce qu’il ait la même position par rapport aux contrôles par défaut que le contrôle **stc32** . Pour faire de la place pour ces nouveaux contrôles, le système ajoute l’espace à gauche, à droite, en bas et en haut de la boîte de dialogue par défaut, si nécessaire.

Le système exige que la procédure de hook traite tous les messages destinés à la boîte de dialogue personnalisée et envoie donc les mêmes messages de fenêtre à la procédure de hook que pour toute autre procédure de la boîte de dialogue. Par exemple, la procédure de hook reçoit des messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) lorsque l’utilisateur clique sur les contrôles de bouton dans la boîte de dialogue personnalisée. La procédure de raccordement est chargée d’initialiser ces contrôles et de récupérer les valeurs des contrôles lorsque la boîte de dialogue est fermée. Notez que lorsque la procédure de hook reçoit le message [**WM \_ INITDIALOG**](wm-initdialog.md) , le système n’a pas encore déplacé les contrôles vers leurs positions finales.

La procédure de boîte de dialogue par défaut gère les messages de tous les contrôles dans la boîte de dialogue par défaut, mais la procédure de hook reçoit les messages de notification pour les actions de l’utilisateur sur ces contrôles, comme décrit dans [procédures de hook de style Explorateur](#explorer-style-hook-procedures).

## <a name="explorer-style-control-identifiers"></a>Identificateurs de contrôle Explorer-Style

Le kit de développement logiciel (SDK) Windows fournit le modèle de boîte de dialogue par défaut pour les anciennes boîtes de dialogue, mais il n’inclut pas le modèle par défaut pour les boîtes de dialogue de style Explorateur. Cela est dû au fait que les boîtes de dialogue de style Explorateur vous permettent d’ajouter vos propres contrôles, mais ne prennent pas en charge la modification du modèle pour les contrôles standard. Toutefois, dans certains cas, vous devrez peut-être connaître les identificateurs de contrôle utilisés dans les modèles par défaut. Par exemple, les messages [**CDM \_ HIDECONTROL**](cdm-hidecontrol.md) et [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md) requièrent un identificateur de contrôle.

Le tableau suivant présente les identificateurs des contrôles standard dans les boîtes de dialogue **ouvrir** et **Enregistrer sous** de style Explorateur. Les identificateurs sont des constantes définies dans Dlgs. h et winuser. h.



| Identificateur de contrôle | Description du contrôle                                                                                                                                                                                                                                                                        |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **chx1**           | Case à cocher en lecture seule                                                                                                                                                                                                                                                                    |
| **cmb1**           | Zone de liste déroulante déroulante qui affiche la liste des filtres de type de fichier                                                                                                                                                                                                                            |
| **stc2**           | Étiquette de la zone de liste déroulante **cmb1**                                                                                                                                                                                                                                                           |
| **cmb2**           | Zone de liste déroulante déroulante qui affiche le lecteur ou le dossier actif, et qui permet à l’utilisateur de sélectionner un lecteur ou un dossier à ouvrir                                                                                                                                                                |
| **stc4**           | Étiquette de la zone de liste déroulante **cmb2**                                                                                                                                                                                                                                                           |
| **cmb13**          | Zone de liste déroulante déroulante qui affiche le nom du fichier actif, permet à l’utilisateur de taper le nom d’un fichier à ouvrir et sélectionne un fichier qui a été ouvert ou enregistré récemment. C’est le cas pour les applications compatibles avec l’Explorateur antérieures sans le modèle de raccordement ou de boîte de dialogue. Comparer à **edt1**. |
| **edt1**           | Contrôle d’édition qui affiche le nom du fichier actif, ou permet à l’utilisateur de taper le nom du fichier à ouvrir. Comparer à **cmb13**.                                                                                                                                                  |
| **stc3**           | Étiquette pour la zone de liste déroulante **cmb13** et le contrôle d’édition edt1                                                                                                                                                                                                                                |
| **lst1**           | Zone de liste qui affiche le contenu du lecteur ou du dossier actif                                                                                                                                                                                                                         |
| **stc1**           | Étiquette de la zone de liste **lst1**                                                                                                                                                                                                                                                            |
| **IDOK**           | Bouton de commande **OK** (bouton de commande)                                                                                                                                                                                                                                                    |
| **IDCANCEL**       | Bouton de commande **Annuler** (bouton de commande)                                                                                                                                                                                                                                                |
| **pshHelp**        | Bouton de commande **d’aide** (bouton de commande)                                                                                                                                                                                                                                                  |



 

## <a name="customizing-old-style-dialog-boxes"></a>Personnalisation des boîtes de dialogue Old-Style

Vous pouvez personnaliser une boîte de dialogue **ouvrir** ou **Enregistrer sous** à l’ancien style en fournissant une procédure de hook [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) qui reçoit des messages ou des notifications destinés à la procédure de boîte de dialogue par défaut. Vous pouvez également fournir un modèle personnalisé à utiliser à la place du modèle par défaut. Les procédures de hook et les modèles utilisés avec les anciennes boîtes de dialogue sont similaires à ceux utilisés avec les autres boîtes de dialogue courantes. Pour plus d’informations, consultez [procédures de Hook pour les boîtes de dialogue communes](customizing-common-dialog-boxes.md) et les [modèles personnalisés](customizing-common-dialog-boxes.md).

Pour activer une procédure de Hook pour une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style ancien, utilisez la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) lors de la création de la boîte de dialogue. Définissez l' **indicateur OFN \_ ENABLEHOOK** dans le membre **Flags** et spécifiez l’adresse d’une procédure de hook [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) dans le membre **lpfnHook** . La procédure de boîte de dialogue envoie un message [**WM \_ INITDIALOG**](wm-initdialog.md) à la procédure de raccordement avec le paramètre *param* défini sur l’adresse de la structure **OpenFileName** utilisée pour initialiser la boîte de dialogue.

Vous pouvez utiliser la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) pour spécifier un modèle personnalisé pour la boîte de dialogue **ouvrir** ou **Enregistrer sous** à utiliser à la place du modèle par défaut. Si votre modèle personnalisé est une ressource dans une application ou une bibliothèque de liens dynamiques, définissez l’indicateur **OFN \_ ENABLETEMPLATE** dans le membre **Flags** et utilisez les membres **HINSTANCE** et **lpTemplateName** de la structure pour identifier le module et le nom de la ressource. Si votre modèle personnalisé est déjà en mémoire, définissez l’indicateur **OFN \_ ENABLETEMPLATEHANDLE** et utilisez le membre **HINSTANCE** pour identifier l’objet mémoire qui contient le modèle. Créez le modèle personnalisé en modifiant le modèle par défaut spécifié dans le fichier FileOpen. dlg. Les identificateurs de contrôle utilisés dans les modèles de boîte de dialogue Rechercher et remplacer par défaut sont définis dans le fichier Dlgs. h.

Par défaut, les fonctions [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) et [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) affichent les boîtes de dialogue de style Explorateur. Si vous souhaitez afficher une boîte de dialogue de style ancien, vous devez fournir une procédure de hook [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) et vérifier que l’indicateur **OFN \_ Explorer** n’est pas défini dans le membre **Flags** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .

Si vous définissez l’indicateur **OFN \_ Explorer** , le système traite une procédure de raccordement ou un modèle personnalisé en tant que personnalisation de type Explorateur. Pour plus d’informations sur la personnalisation d’une boîte de dialogue de style Explorateur, consultez [modèles personnalisés de style Explorateur](#explorer-style-custom-templates).

## <a name="see-also"></a>Voir aussi

* [Exemple de fichier en cours d’utilisation](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)
