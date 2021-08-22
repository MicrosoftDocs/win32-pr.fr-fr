---
description: la table MsiEmbeddedUI définit une interface utilisateur incorporée dans le package Windows Installer.
ms.assetid: d4176f99-e819-4b5a-bd06-1a2965891f9a
title: Table MsiEmbeddedUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7357a0b5aa1de2218eefb58fa85fbe374e9796ad0aaa94946743f1c51d9c8daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012947"
---
# <a name="msiembeddedui-table"></a>Table MsiEmbeddedUI

la table MsiEmbeddedUI définit une interface utilisateur incorporée dans le package Windows Installer.

**[Windows Installer 4,0 ou version antérieure](not-supported-in-windows-installer-4-0.md):** Non pris en charge. cette table est disponible à partir de Windows Installer 4,5.

La table MsiEmbeddedUI contient les colonnes suivantes.



| Colonne        | Type                               | Clé | Nullable |
|---------------|------------------------------------|-----|----------|
| MsiEmbeddedUI | [Identificateur](identifier.md)       | O   | N        |
| FileName      | [Text](text.md)                   | N   | N        |
| Attributs    | [Integer](integer.md)             | N   | N        |
| MessageFilter | [DoubleInteger](doubleinteger.md) | N   | O        |
| Données          | [Binaire](binary.md)               | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="MsiEmbeddedUI"></span><span id="msiembeddedui"></span><span id="MSIEMBEDDEDUI"></span>MsiEmbeddedUI
</dt> <dd>

Clé primaire de la table.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension
</dt> <dd>

Nom du fichier qui reçoit les informations binaires dans la colonne de données. Le nom du fichier est requis pour inclure une extension. Par exemple, le nom *embeddedui.dll* est acceptable, mais *embeddedui* est inacceptable. Le nom peut être localisé. Ce champ peut contenir un nom de fichier abrégé ou un nom de fichier long, mais il ne peut pas contenir les deux. Le format de ce champ est semblable au type de données de la colonne de [nom](filename.md) de fichier, sauf que le séparateur de barre verticale ( \| ) pour la syntaxe de nom de fichier ou de nom de fichier long n’est pas disponible. Étant donné que certains serveurs Web peuvent respecter la casse, le nom de fichier doit correspondre exactement à la casse des fichiers sources pour garantir la prise en charge des téléchargements Internet.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

Informations sur les données de la colonne de données. La valeur de ce champ peut contenir une ou plusieurs des constantes suivantes.



| Constante                      | Valeur hexadécimale | Decimal | Signification                                                                                                                                                                                                                          |
|-------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aucun                          | 0x00        | 0       | Le fichier n’est pas le fichier DLL de l’interface utilisateur. Il peut s’agir d’un fichier de ressources utilisé par l’interface utilisateur.                                                                                                                       |
| **msidbEmbeddedUI**           | 0x01        | 1       | Fichier DLL principal de l’interface utilisateur. Une seule ligne de la table ne peut pas être marquée avec cet attribut. Si plusieurs lignes sont marquées avec cet attribut, il s’agit d’une erreur et il n’est pas possible de garantir la DLL utilisée. |
| **msidbEmbeddedHandlesBasic** | 0x02        | 2       | Permet au programme d’installation d’appeler l’interface utilisateur incorporée pendant une installation de base au niveau de l’interface utilisateur. Le programme d’installation ignore cet attribut s’il n’est pas associé à l’attribut **msidbEmbeddedUI** .                                         |



 

</dd> <dt>

<span id="MessageFilter"></span><span id="messagefilter"></span><span id="MESSAGEFILTER"></span>MessageFilter
</dt> <dd>

Spécifie les types de messages envoyés à la DLL de l’interface utilisateur. Cette colonne ne concerne que les lignes avec l’attribut **msidbEmbeddedUI** . Ce champ doit avoir la valeur null si une ligne fait référence à un fichier de ressources et que la valeur d’attribut est null. Si une ligne fait référence à une DLL d’interface utilisateur, la valeur de cette colonne ne doit pas être null.

La valeur de cette colonne peut être une combinaison des valeurs suivantes. Le programme d’installation ignore toutes les autres valeurs.



| Constante                           | Valeur hexadécimale | Decimal   | Description                                                                                                  |
|------------------------------------|-------------|-----------|--------------------------------------------------------------------------------------------------------------|
| **INSTALLLOGMODE \_ FATALEXIT**      | 0x00001     | 1         | Fin prématurée.                                                                                       |
| **\_erreur INSTALLLOGMODE**          | 0x00002     | 2         | Messages d’erreur.                                                                                              |
| **\_Avertissement INSTALLLOGMODE**        | 0x00004     | 4         | Messages d’avertissement.                                                                                            |
| **\_utilisateur INSTALLLOGMODE**           | 0x00008     | 8         | Messages utilisateur.                                                                                               |
| **\_informations INSTALLLOGMODE**           | 0x00010     | 16        | Messages d’État non journalisés.                                                                                    |
| **INSTALLLOGMODE \_ FILESINUSE**     | 0x00020     | 32        | Fichiers en cours d’utilisation.                                                                                 |
| **INSTALLLOGMODE \_ RESOLVESOURCE**  | 0x00040     | 64        | Demandes de résolution de source.                                                                                  |
| **INSTALLLOGMODE \_ OUTOFDISKSPACE** | 0x00080     | 128       | Messages d’espace disque.                                                                                         |
| **INSTALLLOGMODE \_ ACTIONSTART**    | 0x00100     | 256       | Messages de début d’action.                                                                                       |
| **INSTALLLOGMODE \_ ACTIONDATA**     | 0x00200     | 512       | Messages de données d’action.                                                                                        |
| **progression de INSTALLLOGMODE \_**       | 0x00400     | 1 024      | Messages de progression.                                                                                           |
| **INSTALLLOGMODE \_ COMMONDATA**     | 0x00800     | 2 048      | Messages d’initialisation de l’interface utilisateur.                                                                                  |
| **initialisation de INSTALLLOGMODE \_**     | 0x01000     | 4096      | Messages de démarrage de l’interface utilisateur envoyés lors du démarrage de l’installation d’un produit.                                            |
| **INSTALLLOGMODE \_ Terminate**      | 0x02000     | 8 192      | Messages d’arrêt de l’interface utilisateur envoyés une fois l’installation du produit terminée.                                         |
| **INSTALLLOGMODE, \_ SHOWDIALOG**     | 0x04000     | 16384     | Messages envoyés avant l’affichage de la boîte de dialogue de l’interface utilisateur.                                                             |
| **INSTALLLOGMODE \_ RMFILESINUSE**   | 0x02000000  | 33554432  | Fichiers en cours d’utilisation.                                                                                 |
| **INSTALLLOGMODE \_ INSTALLSTART**   | 0x04000000  | 67108864  | L’installation du produit commence. Le message contient les ProductName et ProductCode du produit.              |
| **INSTALLLOGMODE \_ INSTALLEND**     | 0x08000000  | 134217728 | L’installation du produit se termine. Le message contient le ProductName, le ProductCode et la valeur de retour du produit. |



 

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée
</dt> <dd>

Cette colonne contient des informations binaires. Si le champ d’attribut est marqué avec l’attribut **msidbEmbeddedUI** , les informations contenues dans ce champ doivent être une dll. Si le champ d’attribut n’est pas l’attribut **msidbEmbeddedUI** , les informations contenues dans ce champ peuvent être un fichier de ressources dans n’importe quel format.

</dd> </dl>

## <a name="remarks"></a>Remarques

pour utiliser une interface utilisateur incorporée, le développeur du programme d’installation doit créer cette fonctionnalité dans le package Windows Installer. La table MsiEmbeddedUI définit l’interface utilisateur incorporée. La DLL de l’interface utilisateur incorporée doit exporter les fonctions *InitializeEmbeddedUI*, *EmbeddedUIHandler* et *ShutdownEmbeddedUI* . les Packages qui ne prennent pas en charge une interface utilisateur incorporée peuvent utiliser l’interface utilisateur interne Windows Installer.

pour exécuter les [outils de débogage pour Windows](https://www.microsoft.com/?ref=go) sur une interface utilisateur incorporée, utilisez les techniques décrites dans [débogage des Actions personnalisées](debugging-custom-actions.md). Définissez la valeur de MsiBreak sur MsiEmbeddedUI.

Pour obtenir un exemple d’interface utilisateur personnalisée incorporée, consultez [utilisation d’une interface utilisateur incorporée](using-an-embedded-ui.md).

 

 



