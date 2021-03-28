---
description: Quand l’utilisateur clique avec le bouton droit sur un membre d’un type de fichier pour afficher la feuille de propriétés propriétés, l’interpréteur de commandes appelle les gestionnaires de feuille de propriétés qui sont inscrits pour le type de fichier. Chaque gestionnaire peut ajouter une page personnalisée à la feuille de propriétés par défaut.
title: Comment inscrire et implémenter un gestionnaire de feuille de propriétés pour un type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991556"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a>Comment inscrire et implémenter un gestionnaire de feuille de propriétés pour un type de fichier

Quand l’utilisateur clique avec le bouton droit sur un membre d’un type de fichier pour afficher la feuille de propriétés propriétés, l’interpréteur de commandes appelle les gestionnaires de feuille de propriétés qui sont inscrits pour le type de fichier. Chaque gestionnaire peut ajouter une page personnalisée à la feuille de propriétés par défaut.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   Shell

### <a name="prerequisites"></a>Prérequis

-   Compréhension des menus contextuels

## <a name="instructions"></a>Instructions

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a>Étape 1 : inscription d’un gestionnaire de feuille de propriétés pour un type de fichier

En plus de l’inscription du modèle COM (Component Object Model) normal, ajoutez une sous-clé **PropertySheetHandlers** à la sous-clé **shellex** de la clé ProgID de l’application associée au type de fichier. Créez une sous-clé de **PropertySheetHandlers** avec le nom du gestionnaire et définissez la valeur par défaut sur la forme de chaîne du GUID de l’identificateur de classe (CLSID) du gestionnaire de feuilles de propriétés.

Pour ajouter plusieurs pages à la feuille de propriétés, inscrivez un gestionnaire pour chaque page. Le nombre maximal de pages qu’une feuille de propriétés peut prendre en charge est 32. Pour inscrire plusieurs gestionnaires, créez une clé sous la clé **shellex** pour chaque gestionnaire, avec la valeur par défaut définie sur le GUID CLSID du gestionnaire. Il n’est pas nécessaire de créer un objet distinct pour chaque gestionnaire, ce qui signifie que plusieurs gestionnaires peuvent tous avoir la même valeur GUID. Les pages s’affichent dans l’ordre dans lequel leurs clés sont répertoriées sous **shellex**.

L’exemple suivant illustre une entrée de Registre qui active deux gestionnaires d’extension de feuille de propriétés pour un exemple de type de fichier. MYP. Dans cet exemple, un objet distinct est utilisé pour chaque page, mais un seul objet peut également être utilisé pour les deux.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a>Étape 2 : implémentation d’un gestionnaire de feuille de propriétés pour un type de fichier

En plus de l’implémentation générale décrite dans [Comment fonctionnent les gestionnaires de feuille de propriétés](propsheet-handlers.md), un gestionnaire de feuille de propriétés pour un type de fichier doit également avoir une implémentation appropriée de l’interface [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Seule la méthode [**IShellPropSheetExt :: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) a besoin d’une implémentation qui n’est pas un jeton. L’interpréteur de commandes n’appelle pas [**IShellPropSheetExt :: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).

La méthode [**IShellPropSheetExt :: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) permet à un gestionnaire de feuilles de propriétés d’ajouter une page à une feuille de propriétés. La méthode a deux paramètres d’entrée. Le premier, *lpfnAddPage*, est un pointeur vers une fonction de rappel [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) qui est utilisé pour fournir l’interpréteur de commandes avec les informations nécessaires pour ajouter la page à la feuille de propriétés. La seconde, *lParam*, est une valeur définie par l’interpréteur de commandes qui n’est pas traitée par le gestionnaire. Il est simplement renvoyé à l’interpréteur de commandes lorsque la fonction de rappel est appelée.

La procédure générale pour l’implémentation de [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) est la suivante.

**Implémentation de la méthode AddPages**

1.  Assignez des valeurs appropriées aux membres d’une structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) . En particulier :
    -   Assignez la variable qui contient le décompte de références du gestionnaire au membre **pcRefParent** . Cette pratique empêche l’objet gestionnaire d’être déchargé pendant que la feuille de propriétés est toujours affichée.
    -   Vous pouvez également implémenter une fonction de rappel [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) et assigner son pointeur à un membre **pfnCallback** . Cette fonction est appelée lorsque la page est créée et lorsqu’elle est sur le lieu d’être détruite.
2.  Créez le handle HPAGE de la page en passant la structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) à la fonction [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) .
3.  Appelez la fonction vers laquelle pointe *lpfnAddPage*. Définissez son premier paramètre sur le handle HPAGE créé à l’étape précédente. Affectez à son deuxième paramètre la valeur *lParam* qui a été transmise à [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) par l’interpréteur de commandes.
4.  Tous les messages associés à la page sont transmis à la procédure de boîte de dialogue qui a été assignée au membre **pfnDlgProc** de la structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .
5.  Si vous avez affecté une fonction de rappel [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) à **pfnCallback**, elle est appelée lorsque la page va être détruite. Votre gestionnaire peut ensuite effectuer les opérations de nettoyage nécessaires, telles que la libération des références qu’il contient.

L’exemple de code suivant illustre une implémentation simple de [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) .


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



La variable **g \_ HINST** est le handle d’instance de la dll et IDD \_ PAGEDLG est l’ID de ressource du modèle de boîte de dialogue de la page. La fonction **PageDlgProc** est la procédure de boîte de dialogue qui gère les messages de la page. La variable **g \_ DllRefCount** contient le nombre de références de l’objet. La méthode [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) appelle [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) pour incrémenter le nombre. Toutefois, le décompte de références est libéré par la fonction de rappel, **PageCallbackProc**, lorsque la page va être détruite.

## <a name="remarks"></a>Notes

Pour obtenir une présentation générale de l’inscription des gestionnaires d’extensions de Shell, consultez [création de gestionnaires d’extensions de Shell](handlers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
