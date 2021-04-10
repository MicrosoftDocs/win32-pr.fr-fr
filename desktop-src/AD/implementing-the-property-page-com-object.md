---
title: Implémentation de l’objet COM de la page de propriétés
description: Une extension de feuille de propriétés est un objet COM implémenté en tant que serveur in-proc.
ms.assetid: 77a71086-1949-4828-801e-073ea5a6838b
ms.tgt_platform: multiple
keywords:
- Implémentation de l’objet COM de la page de propriétés
- Objet COM page de propriétés, implémentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55962002ca059ad6e9c137925d1ba21ba9adc513
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842070"
---
# <a name="implementing-the-property-page-com-object"></a>Implémentation de l’objet COM de la page de propriétés

Une extension de feuille de propriétés est un objet COM implémenté en tant que serveur in-proc. L’extension de la feuille de propriétés doit implémenter les interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) et [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Une extension de feuille de propriétés est instanciée lorsque l’utilisateur affiche la feuille de propriétés d’un objet d’une classe pour laquelle l’extension de la feuille de propriétés a été inscrite dans le spécificateur d’affichage de la classe.

-   [Implémentation de IShellExtInit](#implementing-ishellextinit)
-   [Implémentation de IShellPropSheetExt](#implementing-ishellpropsheetext)
-   [Passage de l’objet d’extension à la page de propriétés](#passing-the-extension-object-to-the-property-page)
-   [Utilisation de l’objet de notification](#working-with-the-notification-object)
-   [Divers](#miscellaneous)
-   [Feuilles de propriétés à sélection multiple](#multiple-selection-property-sheets)
-   [Nouveauté de Windows Server 2003](#new-with-windows-server-2003)
-   [Rubriques connexes](#related-topics)

## <a name="implementing-ishellextinit"></a>Implémentation de IShellExtInit

Après l’instanciation de l’objet COM de l’extension de feuille de propriétés, la méthode [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) est appelée. **IShellExtInit :: Initialize** fournit l’extension de la feuille de propriétés avec un objet [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) qui contient des données relatives à l’objet d’annuaire que la feuille de propriétés applique.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contient des données au format [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) . Le format de données **CFSTR \_ DSOBJECTNAMES** est un **HGLOBAL** qui contient une structure [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) . La structure **DSOBJECTNAMES** contient des données d’objet d’annuaire que l’extension de feuille de propriétés applique.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contient également des données au format [**CFSTR \_ DS \_ Display \_ spec \_ options**](cfstr-ds-display-spec-options.md) . Le format de données **CFSTR \_ DS \_ Display \_ spec \_ options** est un **HGLOBAL** qui contient une structure [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) . Le **DSDISPLAYSPECOPTIONS** contient des données de configuration utilisables par l’extension.

Si une valeur autre que **S \_ OK** est retournée à partir de [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), la feuille de propriétés n’est pas affichée.

Les paramètres *pidlFolder* et *hkeyProgID* de la méthode [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) ne sont pas utilisés.

Le pointeur [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) peut être enregistré par l’extension en incrémentant le décompte de références de l' **IDataObject**. Cette interface doit être libérée lorsque vous n’en avez plus besoin.

## <a name="implementing-ishellpropsheetext"></a>Implémentation de IShellPropSheetExt

Après que [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) retourne, la méthode [**IShellPropSheetExt :: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) est appelée. L’extension de la feuille de propriétés doit ajouter la ou les pages pendant cette méthode. Une page de propriétés est créée en remplissant une structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) , puis en passant cette structure à la fonction [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . La page de propriétés est ensuite ajoutée à la feuille de propriétés en appelant la fonction de rappel transmise à **IShellPropSheetExt :: AddPages** dans le paramètre *lpfnAddPage* .

Si une valeur autre que **S \_ OK** est retournée à partir de [**IShellPropSheetExt :: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages), la feuille de propriétés n’est pas affichée.

Si l’extension de la feuille de propriétés n’est pas requise pour ajouter des pages à la feuille de propriétés, elle ne doit pas appeler la fonction de rappel transmise à [**IShellPropSheetExt :: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) dans le paramètre *lpfnAddPage* .

La méthode [**IShellPropSheetExt :: ReplacePage**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) n’est pas utilisée.

## <a name="passing-the-extension-object-to-the-property-page"></a>Passage de l’objet d’extension à la page de propriétés

L’objet d’extension de la feuille de propriétés est indépendant de la page de propriétés. Dans de nombreux cas, il est préférable d’être en mesure d’utiliser l’objet d’extension, ou un autre objet, à partir de la page de propriétés. Pour ce faire, définissez le membre **lParam** de la structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) sur le pointeur d’objet. La page de propriétés peut ensuite récupérer cette valeur lors du traitement du message [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) . Pour une page de propriétés, le paramètre *lParam* du message **WM \_ INITDIALOG** est un pointeur vers la structure **PROPSHEETPAGE** . Récupérez le pointeur d’objet en castant le *lParam* du message **WM \_ INITDIALOG** en pointeur **PROPSHEETPAGE** , puis en récupérant le membre **lParam** de la structure **PROPSHEETPAGE** .

L’exemple de code C++ suivant montre comment passer un objet à une page de propriétés.


```C++
case WM_INITDIALOG:
    {
        LPPROPSHEETPAGE pPage = (LPPROPSHEETPAGE)lParam;

        if(NULL != pPage)
        {
            CPropSheetExt *pPropSheetExt;
            pPropSheetExt = (CPropSheetExt*)pPage->lParam;

            if(pPropSheetExt)
            {
                return pPropSheetExt>OnInitDialog(wParam, lParam);
            }
        }
    }
    break;
```



Sachez qu’après l’appel de [**IShellPropSheetExt :: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) , la feuille de propriétés libère l’objet d’extension de la feuille de propriétés et ne l’utilise jamais. Cela signifie que l’objet d’extension est supprimé avant l’affichage de la page de propriétés. Lorsque la page tente d’accéder au pointeur d’objet, la mémoire est libérée et le pointeur n’est pas valide. Pour corriger cela, incrémentez le décompte de références pour l’objet d’extension lorsque la page est ajoutée, puis libérez l’objet lorsque la boîte de dialogue de la page de propriétés est détruite. Cela crée un autre problème, car la boîte de dialogue page de propriétés n’est pas créée tant que la page n’est pas affichée pour la première fois. Si l’utilisateur ne sélectionne jamais la page d’extension, la page n’est jamais créée ni détruite. Cela a pour effet que l’objet d’extension n’est jamais libéré, ce qui entraîne une fuite de mémoire. Pour éviter cela, implémentez une fonction de rappel de page de propriétés. Pour ce faire, ajoutez l' **indicateur PSP \_ USECALLBACK** au membre **DwFlags** de la structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) et définissez le membre **pfnCallback** de la structure **PROPSHEETPAGE** sur l’adresse de la fonction [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) implémentée. Lorsque la fonction **PropSheetPageProc** reçoit la notification de **\_ publication PSPCB** , le paramètre *PPSP* de l' **PropSheetPageProc** contient un pointeur vers la structure **PROPSHEETPAGE** . Le membre **lParam** de la structure **PROPSHEETPAGE** contient le pointeur d’extension qui peut être utilisé pour libérer l’objet.

L’exemple de code C++ suivant montre comment libérer un objet d’extension.


```C++
UINT CALLBACK CPropSheetExt::PageCallbackProc(  HWND hWnd,
                                                UINT uMsg,
                                                LPPROPSHEETPAGE ppsp)
{
    switch(uMsg)
    {
    case PSPCB_CREATE:
        // Must return TRUE to enable the page to be created.
        return TRUE;

    case PSPCB_RELEASE:
        {
            /*
            Release the object. This is called even if the page dialog box was 
            never actually created.
            */
            CPropSheetExt *pPropSheetExt = (CPropSheetExt*)ppsp->lParam;

            if(pPropSheetExt)
            {
                pPropSheetExt->Release();
            }
        }
        break;
    }

    return FALSE;
}
```



## <a name="working-with-the-notification-object"></a>Utilisation de l’objet de notification

Étant donné que les pages de l’extension de la feuille de propriétés sont affichées dans une feuille de propriétés créée par un composant inconnu de l’extension, il est nécessaire d’utiliser un « gestionnaire » pour gérer le transfert de données entre les pages d’extension et la feuille de propriétés. Ce « gestionnaire » est appelé « objet de notification ». L’objet de notification agit comme un modérateur entre les pages individuelles et la feuille de propriétés.

Lorsque l’objet d’extension de la feuille de propriétés est initialisé, l’extension doit créer un objet de notification en appelant [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj), en transmettant l' [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtenu à partir de [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) et le nom d’objet d’annuaire. Il n’est pas nécessaire d’incrémenter le décompte de références de l’interface **IDataObject** , car l’objet de notification créé par la fonction **ADsPropCreateNotifyObj** effectue cette opération. Le descripteur d’objet de notification fourni par **ADsPropCreateNotifyObj** doit être enregistré pour une utilisation ultérieure. **ADsPropCreateNotifyObj** peut être appelé lors de **IShellExtInit :: Initialize** ou [**IShellPropSheetExt :: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Lorsque l’extension de la feuille de propriétés est arrêtée, elle doit envoyer un message de [**\_ \_ \_ sortie de notification WM ADSPROP**](wm-adsprop-notify-exit.md) à l’objet de notification. L’objet de notification se détruit alors lui-même. Cela s’effectue de façon optimale lorsque la fonction [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) reçoit la notification de **\_ publication PSPCB** .

L’extension de la feuille de propriétés peut obtenir des données en plus de celles fournies par le format de presse-papiers [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) en appelant [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo). L’un des avantages de l’utilisation de **ADsPropGetInitInfo** est qu’il fournit un objet [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) utilisé pour travailler par programmation avec l’objet Directory.

> [!Note]  
> Contrairement à la plupart des méthodes et des fonctions COM, [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) n’incrémente pas le nombre de références pour l’objet [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) . Le **IDirectoryObject** ne doit pas être libéré, sauf si le nombre de références est incrémenté manuellement en premier.

 

Lorsque la page de propriétés est créée pour la première fois, l’extension doit inscrire la page avec l’objet de notification en appelant [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) avec le handle de fenêtre de la page.

[**ADsPropCheckIfWritable**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcheckifwritable) est une fonction utilitaire que l’extension de feuille de propriétés peut utiliser pour déterminer si une propriété peut être écrite.

## <a name="miscellaneous"></a>Divers

Le handle de la page de propriétés est passé à la procédure de la boîte de dialogue de la page. La feuille de propriétés étant le parent direct de la page de propriétés, le handle de la feuille de propriétés peut être obtenu en appelant la fonction [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) avec le handle de la page de propriétés.

Lorsque le contenu de la page d’extension change, l’extension doit utiliser la macro [**PropSheet \_ Changed**](/windows/win32/api/prsht/nf-prsht-propsheet_changed) pour notifier la feuille de propriétés des modifications. La feuille de propriétés activera ensuite le bouton appliquer.

## <a name="multiple-selection-property-sheets"></a>Multiple-Selection les feuilles de propriétés

Avec les systèmes d’exploitation Windows Server 2003 et versions ultérieures, le Active Directory composants logiciels enfichables MMC d’administration prennent en charge les extensions de feuille de propriétés pour plusieurs objets d’annuaire. Ces feuilles de propriétés s’affichent lorsque les propriétés sont affichées pour plusieurs éléments à la fois. La principale différence entre une extension de feuille de propriétés à sélection unique et une extension de feuille de propriétés à sélection multiple est que la structure [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) fournie par le format de presse-papiers [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) dans [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) contient plus d’une structure [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

Lorsque l’objet de notification est créé, une extension de feuille de propriétés à sélection multiple doit passer un nom unique fourni par le composant logiciel enfichable au lieu d’un nom créé par l’extension. Pour obtenir le nom unique, demandez le format du presse-papiers [**CFSTR \_ DS \_ MULTISELECTPROPPAGE**](cfstr-ds-multiselectproppage.md) à partir de l' [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtenu auprès de [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Ces données sont un **HGLOBAL** qui contient une chaîne Unicode terminée par le caractère null qui est le nom unique. Ce nom unique est ensuite transmis à la fonction [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) pour créer l’objet de notification. La fonction exemple **CreateADsNotificationObject** dans l' [exemple de code pour l’implémentation de l’objet com de la feuille de propriétés](example-code-for-implementation-of-the-property-sheet-com-object.md) montre comment effectuer cette opération correctement, ainsi que la compatibilité avec les versions antérieures du composant logiciel enfichable qui ne prennent pas en charge les feuilles de propriétés à sélection multiple.

Pour les feuilles de propriétés à sélection multiple, le système se lie uniquement au premier objet dans le tableau [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) . Pour cette raison, [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) fournit uniquement les attributs [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) et en écriture pour le premier objet du tableau. Les autres objets dans le tableau ne sont pas liés à.

Une extension de feuille de propriétés à sélection multiple est inscrite sous l’attribut [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .

## <a name="new-with-windows-server-2003"></a>Nouveauté de Windows Server 2003

Les fonctionnalités suivantes sont nouvelles dans Windows Server 2003.

Si la page de propriétés rencontre une erreur, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) peut être appelée avec les données d’erreur appropriées. **ADsPropSendErrorMessage** stocke tous les messages d’erreur dans une file d’attente. Ces messages seront affichés lors de l’appel suivant de [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) . Quand **ADsPropShowErrorDialog** retourne, les messages mis en file d’attente sont supprimés.

Windows Server 2003 introduit la fonction [**ADsPropSetHwndWithTitle**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwndwithtitle) . Cette fonction est similaire à [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd), mais elle comprend le titre de la page. Cela active la boîte de dialogue d’erreur affichée par [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) pour fournir des données plus utiles à l’utilisateur. Si l’extension de la feuille de propriétés utilise la fonction **ADsPropShowErrorDialog** , l’extension doit utiliser **ADsPropSetHwndWithTitle** au lieu de **ADsPropSetHwnd**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de code pour l’implémentation de l’objet COM de la feuille de propriétés](example-code-for-implementation-of-the-property-sheet-com-object.md)
</dt> </dl>

 

 