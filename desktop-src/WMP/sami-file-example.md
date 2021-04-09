---
title: Exemple de fichier SAMI
description: Exemple de fichier SAMI
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Modèle objet du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- modèle objet, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX Mobile Player Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX, SAMI (Synchronized Accessible Media Interchange)
- Fichiers de Media Interchange (SAMI) synchronisés, fichiers
- SAMI (Synchronized Accessible Media Interchange), fichiers
- SAMI (Synchronized Accessible Media Interchange), exemple de code
- SAMI (Synchronized Accessible Media Interchange), exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9634de52f71b4ca1db151bdf9104c3891c8ce5d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869386"
---
# <a name="sami-file-example"></a><span data-ttu-id="2168c-114">Exemple de fichier SAMI</span><span class="sxs-lookup"><span data-stu-id="2168c-114">SAMI File Example</span></span>

<span data-ttu-id="2168c-115">L’exemple de code suivant est un fichier SAMI complet avec un ensemble de texte de légende fermé et plusieurs déclarations de classe pour le style de texte et la langue de légende.</span><span class="sxs-lookup"><span data-stu-id="2168c-115">The following example code is a complete SAMI file with one set of closed caption text and several class declarations for text style and caption language.</span></span>


```C++
<SAMI>
<HEAD>
   <STYLE TYPE = "text/css">
   <!--
   /* P defines the basic style selector for closed caption paragraph text */
   P {font-family:sans-serif; color:white;}
   /* Source, Small, and Big define additional ID selectors for closed caption text */
   #Source {color: orange; font-family: arial; font-size: 12pt;}
   #Small {Name: SmallTxt; font-size: 8pt; color: yellow;}
   #Big {Name: BigTxt; font-size: 12pt; color: magenta;}
   /* ENUSCC and FRFRCC define language class selectors for closed caption text */
   .ENUSCC {Name: 'English Captions'; lang: en-US; SAMIType: CC;}
   .FRFRCC {Name: 'French Captions'; lang: fr-FR; SAMIType: CC;}
   -->
   </STYLE>
</HEAD>
<BODY>
   <!<entity type="mdash"/>- The closed caption text displays at 1000 milliseconds. -->
   <SYNC Start = 1000>
      <!-- English closed captions -->
      <P Class = ENUSCC ID = Source>Narrator
      <P Class = ENUSCC>Great reason to visit Seattle, brought to you by two out-of-staters.
      <!-- French closed captions -->
      <P Class = FRFRCC ID = Source>Narrateur
      <P Class = FRFRCC>Deux personnes ne venant la r&eacute;gion vous donnent de bonnes raisons de visiter Seattle.
</BODY>
</SAMI>

```



<span data-ttu-id="2168c-116">Les styles définis dans un fichier SAMI sont conformes à la syntaxe du sélecteur CSS standard pour les éléments, les classes et les ID.</span><span class="sxs-lookup"><span data-stu-id="2168c-116">Styles defined within a SAMI file conform to standard CSS selector syntax for elements, classes, and IDs.</span></span> <span data-ttu-id="2168c-117">Dans l’élément BODY, tous les éléments P ont le style défini pour le sélecteur d’élément P dans l’élément STYLE.</span><span class="sxs-lookup"><span data-stu-id="2168c-117">In the BODY element, all P elements have the style defined for the P element selector in the STYLE element.</span></span> <span data-ttu-id="2168c-118">L’attribut Class d’un élément spécifie le langage de cet élément tel que défini par les sélecteurs de classe dans l’élément STYLE (les sélecteurs qui commencent par des points).</span><span class="sxs-lookup"><span data-stu-id="2168c-118">The class attribute of an element specifies the language of that element as defined by the class selectors in the STYLE element (the selectors beginning with periods).</span></span> <span data-ttu-id="2168c-119">Les noms de langage spécifiés par les sélecteurs de classe peuvent être n’importe quelle chaîne.</span><span class="sxs-lookup"><span data-stu-id="2168c-119">The language names specified by the class selectors can be any string.</span></span> <span data-ttu-id="2168c-120">Les éléments avec l’attribut ID spécifié ont un style supplémentaire appliqué comme indiqué par les sélecteurs d’ID dans l’élément STYLE (les sélecteurs préfixés par des \# caractères).</span><span class="sxs-lookup"><span data-stu-id="2168c-120">Elements with the ID attribute specified have additional styling applied as indicated by the ID selectors in the STYLE element (the selectors prefixed with \# characters).</span></span>

<span data-ttu-id="2168c-121">Lorsqu’ils sont utilisés conjointement avec le modèle objet du lecteur Windows Media, les sélecteurs de classe correspondent à *ClosedCaption*. Propriété **SAMILang** , qui peut être utilisée pour spécifier la langue des légendes.</span><span class="sxs-lookup"><span data-stu-id="2168c-121">When used in conjunction with the Windows Media Player object model, the class selectors correspond to the *ClosedCaption*.**SAMILang** property, which can be used to specify the language of the captions.</span></span> <span data-ttu-id="2168c-122">Les sélecteurs d’ID correspondent au *ClosedCaption*. Propriété **SAMIStyle** , qui peut être utilisée pour spécifier le style dans lequel les sous-titres apparaîtront.</span><span class="sxs-lookup"><span data-stu-id="2168c-122">The ID selectors correspond to the *ClosedCaption*.**SAMIStyle** property, which can be used to specify the style the captions will appear in.</span></span>

<span data-ttu-id="2168c-123">Pour plus d’informations sur la création de fichiers SAMI, voir présentation de SAMI 1,0 sur le [site Web de Microsoft](/documentation/).</span><span class="sxs-lookup"><span data-stu-id="2168c-123">For more information about creating SAMI files, see Understanding SAMI 1.0 at the [Microsoft website](/documentation/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2168c-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2168c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2168c-125">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="2168c-125">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 