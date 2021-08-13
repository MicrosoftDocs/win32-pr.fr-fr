---
description: La table SelfReg contient des informations sur les modules qui doivent être inscrits automatiquement.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Table SelfReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d00b9f18755cf3284edfd1ba9476b12ba6343c816dbafe84ac3c3676f663f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625505"
---
# <a name="selfreg-table"></a>Table SelfReg

La table SelfReg contient des informations sur les modules qui doivent être inscrits automatiquement. Le programme d’installation appelle la fonction [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) lors de l’installation du module ; elle appelle [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) au cours de la désinstallation du module. Le programme d’installation n’inscrit pas automatiquement les fichiers EXE.

La table SelfReg contient les colonnes suivantes.



| Colonne | Type                         | Clé | Nullable |
|--------|------------------------------|-----|----------|
| fichier\_ | [Identificateur](identifier.md) | O   | N        |
| Coût   | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

Clé externe dans la première colonne de la [table file](file-table.md) indiquant le module qui doit être enregistré.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Coûts
</dt> <dd>

Coût de l’enregistrement du module en octets. Il doit s’agir d’un nombre non négatif.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les auteurs de packages d’installation sont fortement recommandés pour l’utilisation de l’inscription automatique. Au lieu de cela, ils doivent inscrire des modules en créant une ou plusieurs tables fournies par le programme d’installation à cet effet. Pour plus d’informations, consultez [Registry tables Group](registry-tables-group.md). La plupart des avantages offerts par un service d’installation central sont perdus avec l’inscription automatique, car les routines d’auto-inscription ont tendance à masquer les informations de configuration critiques. Voici quelques raisons pour lesquelles éviter l’inscription automatique :

-   La restauration d’une installation avec des modules auto-inscrits ne peut pas être effectuée en toute sécurité à l’aide de [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) , car il n’existe aucun moyen de savoir si les clés auto-inscrites sont utilisées par une autre fonctionnalité ou application.
-   La possibilité d’utiliser la publication est réduite si l’inscription du serveur de classe ou d’extension est effectuée dans les routines d’auto-inscription.
-   Le programme d’installation gère automatiquement les clés HKCR dans les tables du Registre pour les installations par utilisateur ou par ordinateur. Actuellement, les routines [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) ne prennent pas en charge la notion de clé HKCR par utilisateur.
-   Si plusieurs utilisateurs utilisent une application auto-inscrite sur le même ordinateur, chaque utilisateur doit installer l’application la première fois qu’il l’exécute. Dans le cas contraire, le programme d’installation ne peut pas déterminer facilement que les clés de Registre HKCU appropriées existent.
-   La fonction [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) peut se voir refuser l’accès aux ressources réseau telles que les bibliothèques de types si un composant est à la fois spécifié en tant que source d’exécution à partir de la source et est listé dans la table Selfreg. Cela peut entraîner l’échec de l’installation du composant au cours d’une installation administrative.
-   L’inscription automatique des dll est plus sensible aux erreurs de codage, car le nouveau code requis pour [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) est généralement différent pour chaque dll. Utilisez plutôt les tables de Registre dans la base de données pour tirer parti du code existant fourni par le programme d’installation.
-   L’inscription automatique des dll peut parfois être liée à des dll auxiliaires absentes ou dont la version est incorrecte. En revanche, le programme d’installation peut inscrire les dll à l’aide des tables de registre sans dépendance sur l’état actuel du système.

> [!Note]  
> Vous ne pouvez pas spécifier l’ordre dans lequel le programme d’installation enregistre ou annule l’enregistrement automatique des dll à l’aide des actions [SelfRegModules](selfregmodules-action.md) et [SelfUnRegModules](selfunregmodules-action.md) . Consultez [spécification de l’ordre d’inscription automatique](specifying-the-order-of-self-registration.md).

 

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 
