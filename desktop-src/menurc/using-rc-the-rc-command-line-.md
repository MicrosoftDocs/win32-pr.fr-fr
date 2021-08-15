---
title: Utilisation de RC (ligne de commande RC)
description: Pour démarrer RC, utilisez la commande suivante.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e560ebee4312dccc2463caf123f05a5ad9831cd293c9976350e6de7ee13cb64a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971918"
---
# <a name="using-rc-the-rc-command-line"></a>Utilisation de RC (ligne de commande RC)

Pour démarrer RC, utilisez la commande suivante.

Version **RC** \[ *options* \] *fichier de script*

Le paramètre de *fichier de script* spécifie le nom du fichier de définition de ressource qui contient les noms, types, noms de fichiers et descriptions des ressources à compiler.

RC peut générer des fichiers de ressources distincts pour les applications qui ont à la fois des ressources indépendantes du langage et des ressources spécifiques à une langue. Les développeurs peuvent utiliser un [fichier de configuration de ressource](/windows/desktop/Intl/preparing-resources) ou définir des options de ligne de commande pour sélectionner les types de ressources et les éléments qui ne sont pas des ressources localisables du fichier indépendant de la [langue (LN)](/windows/desktop/Intl/mui-resource-management) et qui sont des ressources localisables de fichiers MUI spécifiques à une langue. pour plus d’informations, consultez la [interface utilisateur multilingue](/windows/desktop/Intl/multilingual-user-interface).

Le paramètre *options* peut être une ou plusieurs des options de ligne de commande suivantes.

## <a name="options"></a>Options

<dl> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Affiche la liste des options de ligne de commande.

</dd> <dt>

<span id="_c"></span><span id="_C"></span>**commutateur**
</dt> <dd>

Définit une page de codes utilisée par la conversion NLS.

</dd> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Définit un symbole pour le préprocesseur que vous pouvez tester avec la directive [**\# ifdef**](-ifdef.md) .

</dd> <dt>

<span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/FM** *mresname*
</dt> <dd>

RC crée un indépendant de la langue. Fichier RES et un fichier dépendant de la langue (MUI). Fichier RES à l’aide du *fichier de script*. Cette option doit être utilisée avec l’option **/FO** *resName* . RC nomme le indépendant de la langue. RES file *resName. res* et nomme la langue dépendante (MUI). Fichier RES *mresname. res*.

**Windows Server 2003 et Windows XP/2000 :** Cette option n’est pas disponible sans utiliser également les fonctions [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) sur un système mis à jour.

</dd> <dt>

<span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/FO** *resName*
</dt> <dd>

RC crée un. Fichier RES nommé *resName* à l’aide du *fichier de script*.

Si l’option **/FM** *mresname* est également définie, RC crée un indépendant de la langue. Fichier RES et un fichier dépendant de la langue (MUI). Fichier RES.

**Windows Server 2003 et Windows XP/2000 :** Cette option n’est pas disponible sans utiliser également les fonctions [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) sur un système mis à jour.

</dd> <dt>

<span id="_g1"></span><span id="_G1"></span>**/G1**
</dt> <dd>

Si/G1 est défini, RC génère un fichier MUI si la seule ressource localisable incluse dans le fichier MUI est une ressource de version. Si/G1 n’est pas défini, RC ne génère pas de fichier MUI si la seule ressource localisable incluse dans le fichier MUI est une ressource de version.

</dd> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Affiche la liste des options de ligne de commande.

</dd> <dt>

<span id="_I"></span><span id="_i"></span>**/I**
</dt> <dd>

Recherche le répertoire spécifié avant de rechercher dans les répertoires spécifiés par la variable d’environnement INCLUDe.

</dd> <dt>

<span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*
</dt> <dd>

Les types de ressources localisables sont des emplacements dans le pack d’interface utilisateur dépendant du langage. Fichier RES. Si l’option **/q** est également définie, cette option est ignorée et les informations contenues dans le fichier de configuration RC sont prioritaires.

**Windows Server 2003 et Windows XP/2000 :** Cette option n’est pas disponible sans utiliser également les fonctions [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) sur un système mis à jour.

</dd> <dt>

<span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** , *Refrappe*
</dt> <dd>

Le chevauchement des types de ressources par RC place dans le indépendant du langage. RES et le langage dépendant (MUI). Fichiers RES. Les types de ressources spécifiés par l’option **/k** doivent être un sous-ensemble de ceux qui sont spécifiés par l’option **/j** . Par exemple, ? J2? J3? K3 spécifie que RC place le type de ressource 3 à la fois dans les fichiers indépendants de la langue et en fonction de la langue (MUI). Si l’option **/q** est également définie, cette option est ignorée et les informations contenues dans le fichier de configuration RC sont prioritaires.

**Windows Server 2003 et Windows XP/2000 :** Cette option n’est pas disponible sans utiliser également les fonctions [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) sur un système mis à jour.

</dd> <dt>

<span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *ID de langue*
</dt> <dd>

Spécifie la langue par défaut pour la compilation. Par exemple,-l409 équivaut à inclure l’instruction suivante en haut du fichier de script de ressources : `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`

Pour plus d’informations, consultez [identificateurs de langue](/windows/desktop/Intl/language-identifiers).

</dd> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

NULL termine toutes les chaînes dans la table de chaînes.

</dd> <dt>

<span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/Q** *MUI. rcconfig*
</dt> <dd>

Fichier de configuration RC qui suit le format du fichier de configuration RC. Le format de fichier de configuration RC permet aux composants de décrire eux-mêmes des informations sur les ressources telles que le contrôle de version des ressources, le chemin d’accès du fichier MUI, les types de ressources et les éléments. Ce fichier spécifie les ressources qui sont déplacées dans le indépendant de la langue. Fichier RES et les ressources qui sont placées dans la langue (MUI). Fichier RES. Cette option, et les informations fournies dans le fichier de configuration RC, remplacent les options de ligne de commande **/j** et **/k**.

**Windows Server 2003 et Windows XP/2000 :** Cette option n’est pas disponible sans utiliser également les fonctions [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) et [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) sur un système mis à jour.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Ignoré. Fourni pour la compatibilité avec les Makefiles existants.

</dd> <dt>

<span id="_u"></span><span id="_U"></span>**/u.**
</dt> <dd>

Annule la définition d’un symbole pour le préprocesseur.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/f**
</dt> <dd>

Affiche des messages qui indiquent la progression du compilateur.

</dd> <dt>

<span id="_x"></span><span id="_X"></span>**/Path**
</dt> <dd>

Empêche RC de vérifier la variable d’environnement INCLUDe lors de la recherche de fichiers d’en-tête ou de fichiers de ressources.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les options ne respectent pas la casse et un trait d’Union (-) peut être utilisé à la place d’une barre oblique (/). Vous pouvez combiner des options à une seule lettre s’ils n’ont pas besoin de paramètres supplémentaires.

RC ne génère pas de fichier MUI dans les cas suivants.

-   Il n’existe aucune ressource localisable dans le fichier. rc.
-   Le seul ID de langue de ressource spécifié dans le fichier. RC est neutre (0x0).
-   Le fichier. rc contient des ressources spécifiées dans plusieurs langues. L’exception est si le fichier. rc contient deux langues et si une langue est neutre (0x0), RC génère un fichier MUI.

Pour plus d'informations, voir les rubriques suivantes :

-   [Définition des noms pour le préprocesseur](defining-names-for-the-preprocessor.md)
-   [Attribution d’un nouveau nom au fichier de ressources compilé](renaming-the-compiled-resource-file.md)
-   [Recherche de fichiers](searching-for-files.md)
-   [Affichage des messages de progression](displaying-progress-messages.md)
-   [Messages de diagnostic RC](rc-diagnostic-messages.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interface utilisateur multilingue](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 