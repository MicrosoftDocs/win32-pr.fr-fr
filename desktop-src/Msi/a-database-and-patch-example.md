---
description: Une application peut utiliser la fonction MsiOpenDatabase pour ouvrir une base de données d’installation nouvelle ou existante (fichier .msi) ou un package correctif (fichier. msp). L’application vérifie la valeur de retour de MsiOpenDatabase avant d’utiliser le handle de base de données.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Exemple de base de données et de correctif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de816e471bbc3df4ec2970202130dba79267a06cb872e74734de322cba2d68d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997029"
---
# <a name="a-database-and-patch-example"></a>Exemple de base de données et de correctif

Une application peut utiliser la fonction [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) pour ouvrir une base de données d’installation nouvelle ou existante (fichier .msi) ou un package correctif (fichier. msp). L’application vérifie la valeur de retour de **MsiOpenDatabase** avant d’utiliser le handle de base de données.

Les exemples suivants utilisent les variables de type **PMSIHANDLE** définies dans msi. h. Il est recommandé d’utiliser le type **PMSIHANDLE** , car le programme d’installation ferme les objets **PMSIHANDLE** à mesure qu’ils sont hors de portée, tandis que votre application doit fermer **MSIHANDLE** objets en appelant [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle). pour plus d’informations, consultez la section [utiliser PMSIHANDLE à la place du descripteur](windows-installer-best-practices.md) dans la [Windows Installer meilleures pratiques](windows-installer-best-practices.md).

L’exemple suivant ouvre une base de données, sample.msi, en lecture seule. [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) fonctionne uniquement si sample.msi existe dans le répertoire c : \\ test. En cas de réussite, le descripteur de base de données retourné peut être utilisé pour interroger les données du package d’installation à l’aide de [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) et [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



L’exemple suivant ouvre la base de données pour la lecture et l’écriture. Si l’application appelle [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), toutes les modifications apportées à la base de données sont enregistrées. Si l’application n’appelle pas **MsiDatabaseCommit**, aucune modification n’est apportée à la base de données.


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



L’exemple suivant prend une base de données existante, text.msi et crée une nouvelle base de données, newtest.msi. Toutes les modifications apportées peuvent être enregistrées dans la nouvelle base de données en appelant [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). La base de données existante spécifiée dans le paramètre *szDatabasePath* est inchangée.


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



l’exemple suivant ouvre une Windows Installer package correctif (fichier. msp) en lecture seule. le descripteur de correctif renvoyé peut être utilisé pour déterminer les armoires et transformer les sous-stockages inclus dans le package de correctifs par des requêtes sur les tables de [ \_ Flux](-streams-table.md) et de [ \_ stockage](-storages-table.md) .

**Windows Installer 2,0 :** Non pris en charge. à partir de Windows Installer 3,0, l’application peut interroger la [table MsiPatchSequence](msipatchsequence-table.md) présente dans un package correctif qui utilise les nouvelles informations de séquencement de correctifs.


```C++
PMSIHANDLE hDbPatch = 0;
LPCTSTR szPersistMode = MSIDBOPEN_READONLY + MSIDBOPEN_PATCHFILE;
UINT uiStatus4 = MsiOpenDatabase(TEXT("c:\\test\\sample.msp"), szPersistMode, &hDbPatch);
if (ERROR_SUCCESS != uiStatus4)
{
    // process error
    return uiStatus4;
}
```



 

 



