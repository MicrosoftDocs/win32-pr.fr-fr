---
title: À propos du modèle d’objet de texte
description: Cette rubrique fournit une vue d’ensemble globale de TOM.
ms.assetid: e304ec18-ec2e-4ea7-91c6-6f6ab63b72ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b934aab1cbd3dca932b58e4aa99498843cb8cc97
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031970"
---
# <a name="about-text-object-model"></a>À propos du modèle d’objet de texte

Le modèle d’objet de texte (TOM) définit un jeu d’interfaces de manipulation de texte prises en charge à différents degrés par plusieurs solutions de texte Microsoft, y compris le contrôle RichEdit. Cette rubrique fournit une vue d’ensemble globale de TOM. Il aborde les rubriques suivantes.

-   [Objets TOM version 2](#tom-version-2-objects)
-   [TOM, conventions de l’interface](#tom-interface-conventions)
-   [Type tomBool](#the-tombool-type)
-   [Accumulation et génération de mathématiques](#math-buildup-and-build-down)
-   [FORMAT RTF TOM](#tom-rtf)
-   [Recherche de texte enrichi](#finding-rich-text)
-   [Accessibilité TOM](#tom-accessibility)
    -   [Interface de la table d’objets en cours d’exécution](#interface-from-running-object-table)
    -   [Interface des messages de fenêtre](#interface-from-window-messages)
    -   [Méthodes orientées accessibilité](#accessibility-oriented-methods)
-   [Jeux de correspondances de caractères](#character-match-sets)

## <a name="tom-version-2-objects"></a>Objets TOM version 2

TOM version 2 (TOM 2) étend le modèle d’objet de texte d’origine. les nouvelles interfaces sont dérivées des anciennes. L’API TOM mise à jour comprend la prise en charge des nouvelles propriétés de format des caractères et des paragraphes, un modèle de table, une sélection multiple et la prise en charge des objets Inline pour Math et Ruby.

L’objet TOM 2 de niveau supérieur est défini par l’interface [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) , qui a des méthodes pour créer et récupérer des objets plus bas dans la hiérarchie d’objets. Pour un simple traitement de texte brut, vous pouvez obtenir un objet [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) à partir d’un objet **ITextDocument2** et faire tout le reste. Si vous devez ajouter une mise en forme de texte enrichi, vous pouvez obtenir des objets [**ITextFont2**](/windows/desktop/api/Tom/nn-tom-itextfont2) et [**ITextPara2**](/windows/desktop/api/Tom/nn-tom-itextpara2) à partir d’un objet **ITextRange2** . **ITextFont2** fournit l’équivalent de programmation de la boîte de dialogue Format-police de Microsoft Word, et **ITextPara2** fournit l’équivalent de la boîte de dialogue Format de mot-paragraphe.

En plus de ces trois objets de niveau inférieur, TOM 2 a un objet Selection ([**ITextSelection2**](/windows/win32/api/tom/nn-tom-itextselection2)), qui est un objet [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) avec mise en surbrillance de la sélection et certaines méthodes orientées interface utilisateur.

Les objets Range et Selection incluent des méthodes orientées écran qui permettent aux programmes d’examiner le texte à l’écran ou le texte qui peut faire l’objet d’un défilement sur l’écran. Ces fonctionnalités permettent de rendre le texte accessible aux personnes présentant une acuité visuelle réduite, par exemple.

Chaque interface qui a le suffixe 2 hérite de l’interface correspondante sans le suffixe 2. Par exemple, [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) hérite de [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument).

Les objets TOM 2 ont la hiérarchie suivante.

``` syntax
ITextDocument2         Top-level editing object
    ITextRange2        Primary text interface: a range of text
        ITextFont2     Character-attribute interface
        ITextPara2     Paragraph-attribute interface
        ITextRow       Table interface
    ITextSelection2    Screen highlighted text range
        ITextRange2    Selection inherits all range methods
    ITextDisplays      Displays collection (not yet defined)
    ITextStrings       Rich-text strings collection
    ITextStoryRanges2  Enumerator for stories in document
```

Un objet [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) décrit une ou plusieurs plages de texte contiguës appelées *histoires*. Les récits représentent différentes parties d’un document, telles que le texte principal du document, les en-têtes et pieds de page, les notes de bas de page, les annotations et les blocs de travail de texte enrichi. Un bloc-notes est utilisé lors de la conversion entre des expressions mathématiques à format linéaire et un formulaire intégré. Un bloc-notes est également utilisé lors de l’enregistrement du contenu d’une plage qui est la source de copie active lorsque le contenu est sur le lieu d’être modifié.

Un objet [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) est défini par ses décalages de position de caractère de début et de fin et un objet d’histoire. Il n’existe pas indépendamment de son objet Story parent, bien que son texte puisse être copié dans le presse-papiers ou sur d’autres cibles. Un objet de plage de texte est différent de la feuille de calcul et d’autres objets de plage, qui sont définis par d’autres genres de décalages ; par exemple, position de ligne/colonne ou graphique (x, y). Un objet de plage de texte peut se modifier lui-même de différentes façons, peut retourner un doublon de lui-même et il peut être dirigé pour copier ses positions de début et de fin de caractère et son pointeur d’histoire vers la sélection actuelle.

Un objet d’histoire explicite n’est pas nécessaire, car un objet [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) peut toujours être créé pour représenter un récit donné. En particulier, l’objet [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) peut créer un objet [**ITextStoryRanges**](/windows/desktop/api/Tom/nn-tom-itextstoryranges) pour énumérer les récits dans le document en termes de plages avec des valeurs de position de caractère de début et de fin qui décrivent des récits terminés (tels que 0 et **tomForward**).

Avec un objet [**ITextStoryRanges2**](/windows/desktop/api/Tom/nn-tom-itextstoryranges2) , il n’est pas nécessaire d’utiliser un objet d’histoire explicite, car chaque récit est décrit par un objet [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) . En particulier, l’objet [**ITextDocument2**](/windows/desktop/api/tom/nn-tom-itextdocument2) peut créer un objet [**ITextStoryRanges2**](/windows/desktop/api/tom/nn-tom-itextstoryranges2) pour énumérer les récits dans le document en termes de plages avec des valeurs de position de caractère de début et de fin qui décrivent des récits terminés (tels que 0 et **tomForward**).

L’interface [**ITextRow**](/windows/desktop/api/Tom/nn-tom-itextrow) avec les méthodes [**ITextRange :: Move**](/windows/desktop/api/Tom/nf-tom-itextrange-move) et [**ITextRange :: Expand**](/windows/desktop/api/Tom/nf-tom-itextrange-expand) donne la possibilité d’insérer, d’interroger et de modifier des tables.

## <a name="tom-interface-conventions"></a>TOM, conventions de l’interface

Toutes les méthodes TOM retournent des valeurs **HRESULT** . En général, les méthodes TOM retournent les valeurs standard suivantes.

-   \_OUTOFMEMORY E
-   E \_ INVALIDARG
-   \_NOTIMPL E
-   \_FILENOTFOUND E
-   \_ACCESSDENIED E
-   E \_ échec
-   CO \_ - \_ publié
-   NOERROR (identique à S \_ OK)
-   S \_ false

Sachez que si l’instance de modification associée à un objet TOM tel que [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) est supprimée, l’objet Tom devient inutilisable et toutes ses méthodes retournent co \_ E \_ Released.

En plus des valeurs de retour **HRESULT** , de nombreuses méthodes incluent des paramètres out, qui sont des pointeurs utilisés pour retourner des valeurs. Pour toutes les interfaces, vous devez vérifier tous les paramètres de pointeur pour vous assurer qu’ils ne sont pas nuls avant de les utiliser. Si vous transmettez une valeur null à une méthode qui requiert un pointeur valide, la méthode retourne E \_ INVALIDARG. Les pointeurs de sortie facultatifs avec des valeurs NULL sont ignorés.

Utilisez des méthodes avec les préfixes d’extraction et de définition pour récupérer et définir des propriétés. Les variables booléennes utilisent **tomFalse** (0) pour **false** et **tomTrue** (-1) pour **true**.

Les constantes TOM sont définies dans le type d’énumération [**tomConstants**](/windows/win32/api/tom/ne-tom-tomconstants) et commencent par le préfixe *Tom*, par exemple **tomWord**.

## <a name="the-tombool-type"></a>Type tomBool

De nombreuses méthodes TOM utilisent un type spécial de variable appelée « tomBool » pour les attributs de texte enrichi qui ont des États binaires. Le type tomBool est différent du type **booléen** , car il peut prendre quatre valeurs : **tomTrue**, **tomFalse**, **tomToggle** et **tomUndefined**. Les valeurs **tomTrue** et **tomFalse** indiquent true et false. La valeur **tomToggle** est utilisée pour basculer une propriété. La valeur **tomUndefined** , plus traditionnellement appelée NINCH, est une valeur non-entrée spéciale, sans modification, qui fonctionne avec les valeurs long, float et **COLORREF** s. Pour les chaînes, **tomUndefined** (ou NINCH) est représenté par la chaîne NULL. Pour les opérations de définition de propriété, l’utilisation de **tomUndefined** ne modifie pas la propriété cible. Pour les opérations de récupération de propriété, **tomUndefined** signifie que les caractères de la plage ont des valeurs différentes (la case grisée est affichée dans les boîtes de dialogue des propriétés).

## <a name="math-buildup-and-build-down"></a>Accumulation et génération de mathématiques

Vous pouvez utiliser la méthode [**ITextRange2 :: BuildUpMath**](/windows/desktop/api/Tom/nf-tom-itextrange2-buildupmath) pour convertir des expressions mathématiques mises en forme de façon linéaire en versions intégrées. La méthode [**ITextRange2 :: linéarisation**](/windows/desktop/api/Tom/nf-tom-itextrange2-linearize) effectue la conversion inverse, appelée linéarisation ou génération vers le haut, pour convertir en retour les versions intégrées des expressions mathématiques au format linéaire. La fonctionnalité de compilation des mathématiques est utile lorsque vous devez exporter du texte brut ou activer certains types de modification.

## <a name="tom-rtf"></a>FORMAT RTF TOM

Dans TOM, l’échange de texte enrichi peut être effectué par un ensemble d’appels de méthode explicites ou par transferts de texte enrichi au format RTF (Rich Text Format). Cette section fournit des tableaux de mots de contrôle RTF pour les propriétés de paragraphe et pour les propriétés de caractères.

**Mots de contrôle de paragraphe de TOM RTF**

| Mot de contrôle   | Signification                                                                                                                                                                                                                                                                        |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ fi *n*      | Retrait de première ligne (la valeur par défaut est zéro).                                                                                                                                                                                                                                       |
| \\ toujours        | Conserver le paragraphe intact.                                                                                                                                                                                                                                                         |
| \\ conserver       | Conservez le paragraphe suivant.                                                                                                                                                                                                                                                  |
| \\ Li *n*      | Retrait à gauche (la valeur par défaut est zéro).                                                                                                                                                                                                                                             |
| \\ NoLine      | Aucune numérotation des lignes.                                                                                                                                                                                                                                                             |
| \\ nowidctlpar | Désactivez le contrôle veuve/orphelin.                                                                                                                                                                                                                                                 |
| \\ pagebb      | Saut de page avant le paragraphe.                                                                                                                                                                                                                                                   |
| \\ préférez         | Nouveau paragraphe.                                                                                                                                                                                                                                                                 |
| \\ pard        | Réinitialise les propriétés de paragraphe par défaut.                                                                                                                                                                                                                                        |
| \\ QL          | Aligné à gauche (valeur par défaut).                                                                                                                                                                                                                                                    |
| \\ QR          | Aligné à droite.                                                                                                                                                                                                                                                                 |
| \\ qj          | Justifié.                                                                                                                                                                                                                                                                     |
| \\ QC          | Centré.                                                                                                                                                                                                                                                                      |
| \\ RI *n*      | Retrait à droite (la valeur par défaut est zéro).                                                                                                                                                                                                                                            |
| \\ s *n*       | Style *n*.                                                                                                                                                                                                                                                                     |
| \\ sa *n*      | Espace après (la valeur par défaut est zéro).                                                                                                                                                                                                                                             |
| \\ SB *n*      | Espace avant (la valeur par défaut est zéro).                                                                                                                                                                                                                                            |
| \\ SL *n*      | S’il est manquant ou si *n*= 1000, l’interligne est déterminé par le caractère le plus haut de la ligne (espacement sur une seule ligne); Si *n*> zéro, au moins cette taille est utilisée ; Si *n* est < zéro, exactement \| *n* \| est utilisé. L’interligne est un espacement multiligne si \\ slmult 1 suit. |
| \\ slmult *m*  | Suit \\ SL. *m* = zéro : au moins ou exactement l’espacement de ligne comme décrit par \\ SL *n*. *m* = 1 : interligne = *n*/240 fois l’espacement sur une seule ligne.                                                                                                                              |
| \\ to *n*      | Position de l’onglet de la barre, en twips, à partir de la marge de gauche.                                                                                                                                                                                                                              |
| \\ tldot       | Points de suite.                                                                                                                                                                                                                                                               |
| \\ tleq        | Signe égal de la touche Tab.                                                                                                                                                                                                                                                         |
| \\ tlhyph      | Traits d’Union de la touche Tab.                                                                                                                                                                                                                                                            |
| \\ tlth        | Ligne épaisse avec onglets.                                                                                                                                                                                                                                                         |
| \\ tlul        | Trait de soulignement de tabulation.                                                                                                                                                                                                                                                          |
| \\ tqc         | Onglet centré.                                                                                                                                                                                                                                                                  |
| \\ tqdec       | Tabulation décimale.                                                                                                                                                                                                                                                                   |
| \\ tqr         | Onglet Flush-Right.                                                                                                                                                                                                                                                               |
| \\ TX *n*      | Position de l’onglet, en twips, à partir de la marge de gauche.                                                                                                                                                                                                                                  |



 

**Mots de contrôle de format de caractère RTF TOM**

| Mot de contrôle     | Signification                                                                                                                                                                                                                                  |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ animation *n* | Définit le type d’animation sur *n*.                                                                                                                                                                                                              |
| \\ p             | Gras.                                                                                                                                                                                                                                    |
| \\ limitations          | Tout en majuscules.                                                                                                                                                                                                                            |
| \\ CF *n*        | Couleur de premier plan (la valeur par défaut est **tomAutocolor**).                                                                                                                                                                                      |
| \\ CS *n*        | Style de caractère *n*.                                                                                                                                                                                                                     |
| \\ DN *n*        | Position d’indice en demi-points (la valeur par défaut est 6).                                                                                                                                                                                    |
| \\ embo          | En relief.                                                                                                                                                                                                                                |
| \\ f *n*         | Numéro de police, *n* fait référence à une entrée dans la table de polices.                                                                                                                                                                                   |
| \\ FS *n*        | Taille de la police en demi-points (la valeur par défaut est 24).                                                                                                                                                                                            |
| \\ en surbrillance *n* | Couleur d’arrière-plan (la valeur par défaut est **tomAutocolor**).                                                                                                                                                                                      |
| \\ cliqu             | Italique.                                                                                                                                                                                                                                  |
| \\ impr          | Empreinte.                                                                                                                                                                                                                                 |
| \\ lang *n*      | Applique une langue à un caractère. *n* est un nombre correspondant à une langue. Le \\ mot de contrôle simple réinitialise la propriété Language avec la langue définie par \\ deflang *n* dans les propriétés du document.                             |
| \\ nosupersub    | Désactive l’exposant ou l’indice.                                                                                                                                                                                                      |
| \\ outl          | Décrire.                                                                                                                                                                                                                                 |
| \\ traditionnelle         | Réinitialise les propriétés de mise en forme des caractères à une valeur par défaut définie par l’application. Les propriétés de mise en forme des caractères associées (décrites dans la section Propriétés de caractères associées dans la spécification RTF) sont également réinitialisées. |
| \\ scaps         | Petites majuscules.                                                                                                                                                                                                                          |
| \\ Shading          | Style.                                                                                                                                                                                                                                  |
| \\ jaunes        | Barre.                                                                                                                                                                                                                           |
| \\ indice           | Applique un indice à du texte et réduit la taille du point en fonction des informations de police.                                                                                                                                                          |
| \\ silencieux         | Applique un exposant au texte et réduit la taille du point en fonction des informations de police.                                                                                                                                                        |
| \\ UL            | Souligné continu. \\ uL0 désactive tout soulignement.                                                                                                                                                                                  |
| \\ uld           | Soulignement en pointillés.                                                                                                                                                                                                                        |
| \\ uldb          | Double souligné.                                                                                                                                                                                                                        |
| \\ ulnone        | Arrête tout soulignement.                                                                                                                                                                                                                   |
| \\ ulw           | Souligner le mot.                                                                                                                                                                                                                          |
| \\ haut *n*        | Position de l’exposant en demi-point (la valeur par défaut est 6).                                                                                                                                                                                  |
| \\ v             | Texte masqué.                                                                                                                                                                                                                             |



 

## <a name="finding-rich-text"></a>Recherche de texte enrichi

Vous pouvez utiliser les méthodes TOM pour rechercher du texte enrichi tel que défini par une plage de texte. Il est souvent nécessaire de rechercher un tel texte enrichi dans le traitement de texte, bien qu’il n’ait jamais été respecté dans un traitement de texte « ce que vous voyez est ce que vous obtenez » (WYSIWYG). Il existe clairement un plus grand domaine de correspondance de texte enrichi qui permet d’ignorer certaines propriétés de mise en forme de caractères (ou d’inclure la mise en forme des paragraphes et/ou le contenu de l’objet), mais ces généralisations n’entrent pas dans le cadre de cette section.

L’une des finalités de cette fonctionnalité est d’utiliser une boîte de dialogue de **recherche** de texte enrichi pour définir le texte enrichi que vous souhaitez rechercher dans un document. La boîte de dialogue est implémentée à l’aide d’un contrôle RichEdit et les méthodes TOM sont utilisées pour effectuer la recherche dans le document. Vous pouvez copier le texte enrichi souhaité à partir du document dans la boîte de dialogue **Rechercher** , ou le saisir et le mettre en forme directement dans la boîte de dialogue **Rechercher** .

L’exemple suivant montre comment utiliser les méthodes TOM pour rechercher du texte contenant des combinaisons de mise en forme de caractères exactes. L’algorithme recherche le texte brut dans la plage de correspondance, qui est nommée `pr1` . Si le texte brut est trouvé, il est pointé par une période d’évaluation, appelée `pr2` . Ensuite, deux plages de points d’insertion ( `prip1` et `prip2` ) sont utilisées pour parcourir la plage d’évaluation en comparant sa mise en forme de caractères à celle de `pr1` . S’ils correspondent exactement, la plage d’entrée (donnée par `ppr` ) est mise à jour pour pointer vers le texte de la plage d’évaluation et la fonction retourne le nombre de caractères dans la plage correspondante. Deux objets [**ITextFont**](/windows/desktop/api/Tom/nn-tom-itextfont) , `pf1` et `pf2` , sont utilisés dans la comparaison de mise en forme des caractères. Ils sont attachés aux plages de points d’insertion `prip1` et `prip2` .


```
LONG FindRichText (
    ITextRange **ppr,             // Ptr to range to search
    ITextRange *pr1)              // Range with rich text to find
{
    BSTR        bstr;             // pr1 plain-text to search for
    LONG        cch;              // Text string count
    LONG        cch1, cch2;       // tomCharFormat run char counts
    LONG        cchMatch = 0;     // Nothing matched yet
    LONG        cp;               // Handy char position
    LONG        cpFirst1;         // pr1 cpFirst
    LONG        cpFirst2;         // pr2 cpFirst
    ITextFont  *    pf1, *pf      // Fonts corresponding to IPs prip1 and prip2
    ITextRange *pr2;              // Range duplicate to search with
    ITextRange *prip1, *prip      // Insertion points to walk pr1, pr2

    if (!ppr || !*ppr || !pr1)
        return E_INVALIDARG;

    // Initialize range and font objects used in search
    if ((*ppr)->GetDuplicate(&pr2)    != NOERROR ||
        pr1->GetDuplicate(&prip1)     != NOERROR ||
        pr2->GetDuplicate(&prip2)     != NOERROR ||
        prip1->GetFont(&pf1)          != NOERROR ||
        prip2->GetFont(&pf2)          != NOERROR ||
        pr1->GetText(&bstr)           != NOERROR )
    {
        return E_OUTOFMEMORY;
    }

    pr1->GetStart(&cpFirst1);

    // Keep searching till rich text is matched or no more plain-text hits
    while(!cchMatch && pr2->FindText(bstr, tomForward, 0, &cch) == NOERROR)
    {
        pr2->GetStart(&cpFirst2);                 // pr2 is a new trial range
        prip1->SetRange(cpFirst1, cpFirst1);      // Set up IPs to scan match
        prip2->SetRange(cpFirst2, cpFirst2);      //  and trial ranges

        while(cch > 0 &&
            pf1->IsEqual(pf2, NULL) == NOERROR)   // Walk match & trial ranges
        {                                         //  together comparing font
            prip1->GetStart(&cch1);               //  properties
            prip1->Move(tomCharFormat, 1, NULL);
            prip1->GetStart(&cp);
            cch1 = cp - cch1;                     // cch of next match font run

            prip2->GetStart(&cch2);
            prip2->Move(tomCharFormat, 1, NULL);
            prip2->GetStart(&cp);
            cch2 = cp - cch2;                      // cch of next trial font run

            if(cch1 < cch)                         // There is more to compare
            {
                if(cch1 != cch2)                   // Different run lengths:
                    break;                         //  no formatting match
                cch = cch - cch1;                  // Matched format run
            }
            else if(cch2 < cch)                    // Trial range format run too
                break;                             //  short

            else                                   // Both match and trial runs
            {                                      //  reach at least to match
                pr2->GetEnd(&cp);                  //  text end: rich-text match
                (*ppr)->SetRange(cpFirst2, cp)     // Set input range to hit
                cchMatch = cp - cpFirst2;          //  coordinates and return
                break;                             //  length of matched string
            }
        }
    }
    pr2->Release();
    prip1->Release();
    prip2->Release();
    pf1->Release();
    pf2->Release();
    SysFreeString(bstr);

    return cchMatch;
}
```



## <a name="tom-accessibility"></a>Accessibilité TOM

TOM fournit la prise en charge de l’accessibilité via les interfaces [**ITextSelection**](/windows/desktop/api/Tom/nn-tom-itextselection) et [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) . Cette section décrit les méthodes qui sont utiles pour l’accessibilité, ainsi que la façon dont un programme peut déterminer la position de l’écran *x*, *y* d’un objet.

Étant donné que les programmes d’accessibilité basés sur l’interface utilisateur fonctionnent généralement avec l’écran et la souris, il est souvent important de trouver l’interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) correspondante pour l’emplacement actuel de la souris (en coordonnées d’écran). Les sections suivantes présentent deux façons de déterminer l’interface appropriée :

-   [Via la table d’objets en cours d’exécution](#interface-from-running-object-table)
-   Via le message [**em \_ GETOLEINTERFACE**](em-getoleinterface.md) , qui fonctionne pour les instances de modification riches en fenêtres, à condition que le client se trouve dans le même espace de processus (aucun *marshaling* n’est nécessaire)

Pour plus d’informations, consultez la spécification Microsoft Active Accessibility. Après avoir obtenu un objet à partir d’une position d’écran, vous pouvez utiliser pour une interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) et appeler la méthode [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) pour obtenir un objet Range vide au niveau de la CP correspondant à la position de l’écran.

### <a name="interface-from-running-object-table"></a>Interface de la table d’objets en cours d’exécution

Une table ROT (Running Object Table) indique les instances d’objet qui sont actives. En interrogeant cette table, vous pouvez accélérer le processus de connexion d’un client à un objet lorsque l’objet est déjà en cours d’exécution. Pour que les programmes puissent accéder à TOM interfaces par le biais de la table des objets en cours d’exécution, une instance TOM avec une fenêtre doit s’inscrire dans la table ROT à l’aide d’un moniker. Vous construisez le moniker à partir d’une chaîne contenant la valeur hexadécimale de son [**HWND**](/windows/desktop/WinProg/windows-data-types). L’exemple de code suivant montre comment procéder.


```
// This TOM implementation code is executed when a new windowed 
// instance starts up. 
// Variables with leading underscores are members of this class.

HRESULT hr;
OLECHAR szBuf[10];            // Place to put moniker
MONIKER *pmk;

hr = StringCchPrintf(szBuff, 10, "%x", _hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
OleStdRegisterAsRunning(this, pmk, &_dwROTcookie);
....................
 
// Accessibility Client: 
//    Find hwnd for window pointed to by mouse cursor.

GetCursorPos(&pt);
hwnd = WindowFromPoint(pt);

// Look in ROT (running object table) for an object attached to hwnd

hr = StringCchPrintf(szBuff, 10, "%x", hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
CreateBindContext(0, &pbc);
pmk->BindToObject(pbc, NULL, IID_ITextDocument, &pDoc);
pbc->Release();

if( pDoc )
{
    pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
    // ...now do whatever with the range pRange
}
```



### <a name="interface-from-window-messages"></a>Interface des messages de fenêtre

Le message [**em \_ GETOLEINTERFACE**](em-getoleinterface.md) fournit une autre façon d’obtenir une interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pour un objet à une position d’écran donnée. Comme décrit dans [interface à partir de la table d’objets en cours d’exécution](#interface-from-running-object-table), vous recevez un [**HWND**](/windows/desktop/WinProg/windows-data-types) pour la position d’écran, puis vous envoyez ce message à ce **HWND**. Le **message \_ GETOLEINTERFACE em** est spécifique à la modification et retourne un pointeur vers une interface [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) dans la variable adressée par *lParam*.

**Conseil** Si un pointeur est retourné (veillez à définir l’objet sur lequel *lParam* pointe sur null avant d’envoyer le message), vous pouvez appeler sa méthode [**IUnknown :: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir une interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) . L'exemple de code suivant illustre cette approche.


```
    HWND    hwnd;
    ITextDocument *pDoc;
    ITextRange *pRange;
    POINT    pt;
    IUnknown *pUnk = NULL;
    
    GetCursorPos(&pt);
    hwnd = WindowFromPoint(pt);
    SendMessage(hwnd, EM_GETOLEINTERFACE, 0, (LPARAM)&pUnk);
    if(pUnk && 
        pUnk->QueryInterface(IID_ITextDocument, &pDoc) == NOERROR)
    {
        pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
        //  ... continue with rest of program
    }
```



### <a name="accessibility-oriented-methods"></a>Méthodes orientées accessibilité

Certaines méthodes TOM sont particulièrement utiles pour naviguer à l’écran, tandis que les autres méthodes TOM améliorent ce que vous pouvez faire quand vous arrivez aux endroits qui vous intéressent. Le tableau suivant décrit les méthodes les plus utiles.



| Méthode                                                 | Comment il promeut l’accessibilité                                                                                                                                                                 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSelection**](/windows/desktop/api/Tom/nf-tom-itextdocument-getselection)     | Cette méthode obtient la sélection active qui peut être utilisée pour divers objectifs orientés vue, tels que la mise en surbrillance du texte et le défilement.                                                      |
| [**Telle**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) | En cas d’utilisation sur une sélection active, cette méthode est garantie pour obtenir une plage associée à une vue particulière.                                                                                 |
| [**Développez**](/windows/desktop/api/Tom/nf-tom-itextrange-expand)                    | Agrandit une plage de texte de sorte que toutes les unités partielles qu’elle contient soient entièrement contenues. Par exemple, `Expand(tomWindow)` développe la plage pour inclure la partie visible de l’histoire de la plage. |
| [**GetDuplicate**](/windows/desktop/api/Tom/nf-tom-itextrange-getduplicate)        | En cas d’utilisation sur une sélection active, cette méthode est garantie pour obtenir une plage associée à une vue particulière. Consultez la description de [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint).  |
| [**GetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-getpoint)                | Obtient les coordonnées d’écran pour la position du caractère de début ou de fin dans la plage de texte.                                                                                                        |
| [**ScrollIntoView**](/windows/desktop/api/Tom/nf-tom-itextrange-scrollintoview)    | Fait défiler une plage de texte dans la vue.                                                                                                                                                               |
| [**SetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-setpoint)                | Sélectionne du texte à un point spécifié ou jusqu’à un.                                                                                                                                              |



 

## <a name="character-match-sets"></a>Jeux de correspondances de caractères

Le paramètre *Variant* des différentes méthodes **Move** \* dans [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange), comme [**MoveWhile**](/windows/desktop/api/Tom/nf-tom-itextrange-movewhile) et [**MoveUntil**](/windows/desktop/api/Tom/nf-tom-itextrange-moveuntil), peut prendre une chaîne explicite ou un jeu d’index de correspondances de caractères 32 bits. Les index sont définis par des plages Unicode ou des jeux de caractères [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) . La plage Unicode commençant à *n* et de longueur *l* (< 32768) est donnée par l’index *n* + (*l <*< 16) + 0x80000000. Par exemple, les lettres grecques de base sont définies par CR \_ grec = 0x805f0370 et les caractères ASCII imprimables sont définis par CR \_ ASCIIPrint = 0x805e0020. En outre, les méthodes **MoveWhile** et **MoveUntil** vous permettent de contourner rapidement une plage de caractères dans n’importe quel jeu de caractères **GetStringTypeEx** ou dans une plage de caractères qui ne figure pas dans l’un de ces jeux de caractères.

Les jeux [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) sont spécifiés par les valeurs de *Ctype1*, *Ctype2* et *Ctype3*, et sont définis comme suit.



| Cset                 | Signification                          |
|----------------------|----------------------------------|
| *Ctype1*             | Combinaison de \_ types de CTYPE1 CT. |
| *Ctype2* + tomCType2 | N’importe quel \_ type de CTYPE2 CT.             |
| *Ctype3* + tomCType3 | Combinaison de \_ types de CTYPE3 CT. |



 

Plus précisément, *Ctype1* peut être n’importe quelle combinaison des éléments suivants.



| Nom de Ctype1 | Valeur  | Signification                                                           |
|-------------|--------|-------------------------------------------------------------------|
| C1 \_ supérieur   | 0x0001 | Capitale.                                                        |
| C1 \_ inférieur   | 0x0002 | Minuscules.                                                        |
| \_Chiffre C1   | 0x0004 | Chiffres décimaux.                                                   |
| \_Espace C1   | 0x0008 | Espaces.                                                 |
| C1 \_ PUNCT   | 0x0010 | Ponctuation.                                                      |
| C1 \_ CTRL   | 0x0020 | Caractères de contrôle.                                               |
| C1 \_ vide   | 0x0040 | Caractères vides.                                                 |
| C1 \_ XDIGIT  | 0x0080 | Chiffres hexadécimaux.                                               |
| C1 \_ alpha   | 0x0100 | Tout caractère linguistique (alphabétique, syllabaire ou idéographique). |
| C1 \_ défini | 0x0200 | Un caractère défini, mais pas l’un des autres \_ \* types C1.       |



 

Les types *Ctype2* prennent en charge la disposition correcte du texte Unicode. Les attributs de direction sont assignés afin que l’algorithme de disposition bidirectionnelle standardisé par Unicode produise des résultats précis. Ces types s’excluent mutuellement. Pour plus d’informations sur l’utilisation de ces attributs, consultez *la norme Unicode : encodage de caractères dans le monde entier, volumes 1 et 2* Addison-Wesley société de publication : 1991, 1992.



| Nom de CType2          | Valeur | Signification                          |
|----------------------|-------|----------------------------------|
| Sûr              |       |                                  |
| \_LEFTTORIGHT C2      | 0x1   | De gauche à droite.                   |
| C2 \_ RightToLeft      | 0x2   | De droite à gauche                   |
| Très                |       |                                  |
| \_EUROPENUMBER C2     | 0x3   | Numéro européen, chiffre européen. |
| \_EUROPESEPARATOR C2  | 0x4   | Séparateur numérique européen.      |
| \_EUROPETERMINATOR C2 | 0x5   | Terminateur numérique européen.     |
| \_ARABICNUMBER C2     | 0x6   | Nombre arabe.                   |
| \_COMMONSEPARATOR C2  | 0x7   | Séparateur numérique commun.        |
| Neutralisant             |       |                                  |
| \_BLOCKSEPARATOR C2   | 0x8   | Séparateur de bloc.                 |
| \_SEGMENTSEPARATOR C2 | 0x9   | Séparateur de segments.               |
| \_Espace blanc C2       | 0xA   | Espace blanc.                     |
| \_OTHERNEUTRAL C2     | 0xB   | Autres neutres.                  |
| Non applicable :      |       |                                  |
| \_NOTAPPLICABLE C2    | 0x0   | Aucune direction implicite.           |



 

Les types *Ctype3* sont destinés à être des espaces réservés pour les extensions des types POSIX requis pour le traitement de texte général ou pour les fonctions de la bibliothèque C standard.



| Nom de CType3       | Valeur  | Signification                                                             |
|-------------------|--------|---------------------------------------------------------------------|
| Sans \_ espacement C3    | 0x1    | Marque de non-espacement.                                                    |
| Signe \_ DIACRITIQUE C3     | 0x2    | Marque de non-espacement diacritiques.                                          |
| \_VOWELMARK C3     | 0x4    | Marque de non-espacement des voyelles.                                              |
| \_Symbole C3        | 0x8    | Symbole.                                                             |
| C3 \_ Katakana      | 0x10   | Caractère Katakana.                                                 |
| C3 \_ hiragana      | 0x20   | Caractère Hiragana.                                                 |
| C3 \_ demi-chasse     | 0x40   | Caractère à demi-chasse.                                               |
| \_Pleine chasse     | 0x80   | Caractère à pleine chasse.                                               |
| C3, \_ IDÉOGRAMME     | 0x100  | Caractère IDÉOGRAPHIQUE.                                              |
| C3 \_ kachidé       | 0x200  | Caractère kachidé arabe.                                           |
| C3 \_ alpha         | 0x8000 | Tous les caractères linguistiques (alphabétique, syllabe et idéographique). |
| \_NOTAPPLICABLE C3 | 0x0    | Non applicable.                                                     |



 

Un kit de développement de type édition (EDK) peut inclure des définitions d’index *pvar* pour les plages suivantes décrites dans la norme Unicode.



| Jeu de caractères         | Plage Unicode | Jeu de caractères             | Plage Unicode |
|-----------------------|---------------|---------------------------|---------------|
| ASCII                 | 0x0:0x7F      | ANSI                      | 0x0 — 0xFF      |
| ASCIIPrint            | 0x20 — 0x7E     | Latin1                    | 0x20 — 0xFF     |
| Latin1Supp            | 0xa0:0xFF     | LatinXA                   | 0x100 — 0x17f   |
| LatinXB               | 0x180—0x24f   | IPAX                      | 0x250—0x2af   |
| SpaceMod              | 0x2b0—0x2ff   | Fusionn                 | 0x300—0x36f   |
| Grec                 | 0x370—0x3ff   | BasicGreek                | 0x370—0x3cf   |
| GreekSymbols          | 0x3d0—0x3ff   | Cyrillique                  | 0x400 — 0x4ff   |
| Arménien              | 0x530—0x58f   | Hébreu                    | 0x590—0x5ff   |
| BasicHebrew           | 0x5d0—0x5ea   | HebrewXA                  | 0x590—0x5cf   |
| HebrewXB              | 0x5eb—0x5ff   | Arabe                    | 0x600 — 0x6ff   |
| BasicArabic           | 0x600 — 0x652   | ArabicX                   | 0x653—0x6ff   |
| Devangari             | 0x900—0x97f   | Bangla (anciennement bengali) | 0x980—0x9ff   |
| Gurmukhi              | 0xa00—0xa7f   | Goudjrati                  | 0xa80—0xaff   |
| Odia (anciennement Oriya) | 0xb00—0xb7f   | Tamoul                     | 0xb80—0xbff   |
| Teluga                | 0xc00—0xc7f   | Kannada                   | 0xc80—0xcff   |
| Malayalam             | 0xd00—0xd7f   | Thaï                      | 0xe00—0xe7f   |
| Lao                   | 0xe80—0xeff   | GeorgianX                 | 0x10a0—0xa0cf |
| BascGeorgian          | 0x10d0—0x10ff | Jamos                      | 0x1100—0x11ff |
| LatinXAdd             | 0x1e00—0x1eff | GreekX                    | 0x1f00—0x1fff |
| GenPunct              | 0x2000 — 0x206f | Exposant               | 0x2070—0x207f |
| Indice             | 0x2080—0x208f | Superindice            | 0x2070—0x209f |
| Devise              | 0x20a0—0x20cf | CombMarkSym               | 0x20d0—0x20ff |
| Type lettre            | 0x2100—0x214f | NumberForms               | 0x2150—0x218f |
| Flèches                | 0x2190—0x21ff | MathOps                   | 0x2200—0x22ff |
| MiscTech              | 0x2300—0x23ff | CtrlPictures              | 0x2400—0x243f |
| OptCharRecog          | 0x2440—0x245f | EnclAlphaNum              | 0x2460—x24ff  |
| BoxDrawing            | 0x2500—0x257f | BlockElement              | 0x2580—0x259f |
| GeometShapes          | 0x25a0—0x25ff | MiscSymbols               | 0x2600—0x26ff |
| Casseau              | 0x2700—0x27bf | CJKSymPunct               | 0x3000—0x303f |
| Hiragana              | 0x3040—0x309f | Katakana                  | 0x30a0—0x30ff |
| Bopomofo              | 0x3100—0x312f | HangulJamo                | 0x3130—0x318f |
| CJLMisc               | 0x3190—0x319f | EnclCJK                   | 0x3200—0x32ff |
| CJKCompatibl          | 0x3300—0x33ff | IDÉOGRAMME                       | 0x3400—0xabff |
| Hangul                | 0xac00—0xd7ff | UTF16Lead                 | 0xD800 — 0xDBFF |
| UTF16Trail            | 0xDC00 — 0xDFFF | PrivateUse                | 0xe000—0xf800 |
| CJKCompIdeog          | 0xf900—0xfaff | AlphaPres                 | 0xfb00—0xfb4f |
| ArabicPresA           | 0xfb50—0xfdff | CombHalfMark              | 0xfe20—0xfe2f |
| CJKCompForm           | 0xfe30—0xfe4f | SmallFormVar              | 0xfe50—0xfe6f |
| ArabicPresB           | 0xfe70—0xfefe | HalfFullForm              | 0xff00—0xffef |
| Offres spéciales              | 0xfff0—0xfffd |                           |               |



 

 

 