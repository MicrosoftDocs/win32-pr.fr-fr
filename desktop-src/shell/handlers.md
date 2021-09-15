---
description: Les fonctionnalités de l’interpréteur de commandes peuvent être étendues avec des entrées de Registre et des fichiers de .ini.
ms.assetid: 74a81e4f-7357-4901-a118-ba44e8892f25
title: Création de gestionnaires d’extensions d’environnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f3c1684b7491e2ad29fae29f48164ffdd47cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523380"
---
# <a name="creating-shell-extension-handlers"></a>Création de gestionnaires d’extensions d’environnement

Les fonctionnalités de l’interpréteur de commandes peuvent être étendues avec des entrées de Registre et des fichiers de .ini. Bien que cette approche de l’extension de l’interpréteur de commandes soit simple et adaptée à de nombreuses fins, elle est limitée. Par exemple, si vous utilisez le registre pour spécifier une icône personnalisée pour un type de fichier, la même icône s’affiche pour chaque fichier de ce type. L’extension de l’interpréteur de commandes avec le registre ne vous permet pas de faire varier l’icône pour différents fichiers du même type. D’autres aspects de l’interpréteur de commandes, tels que la feuille de propriétés des **Propriétés** qui peuvent être affichées lorsqu’un utilisateur clique avec le bouton droit, ne peuvent pas être modifiés du tout à l’aide du Registre.

Une approche plus puissante et flexible pour étendre l’interpréteur de commandes consiste à implémenter des *gestionnaires d’extensions de Shell*. Ces gestionnaires peuvent être implémentés pour diverses actions que l’interpréteur de commandes peut effectuer. Avant d’entreprendre l’action, l’interpréteur de commandes interroge le gestionnaire d’extensions, en lui donnant la possibilité de modifier l’action. Un gestionnaire d’extensions de menu contextuel est un exemple courant. Si l’une d’elles est implémentée pour un type de fichier, elle est interrogée chaque fois que l’utilisateur clique avec le bouton droit sur l’un des fichiers. Le gestionnaire peut ensuite spécifier des éléments de menu supplémentaires pour chaque fichier, au lieu d’avoir le même ensemble pour le type de fichier entier.

Ce document explique comment implémenter les gestionnaires d’extension qui vous permettent de modifier diverses actions de l’interpréteur de commandes. Les gestionnaires suivants sont associés à un type de fichier particulier et vous permettent de spécifier la base de données fichier par fichier :



| Handler                                               | Description                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestionnaire de menu contextuel](context-menu-handlers.md)    | Appelé avant l’affichage du menu contextuel d’un fichier. Elle vous permet d’ajouter des éléments au menu contextuel, fichier par fichier.                                               |
| [Gestionnaire de données](how-to-create-data-handlers.md)       | Appelé lorsqu’une opération de glisser-déplacer est exécutée sur des objets dragShell. Elle vous permet de fournir des formats de presse-papiers supplémentaires à la cible de déplacement.                        |
| [Supprimer le gestionnaire](how-to-create-drop-handlers.md)       | Appelé lorsqu’un objet de données est déplacé ou déplacé sur un fichier. Elle vous permet de créer un fichier dans une cible de déplacement.                                                          |
| [Gestionnaire d’icône](how-to-create-icon-handlers.md)       | Appelé avant l’affichage de l’icône d’un fichier. Elle vous permet de remplacer l’icône par défaut du fichier par une icône personnalisée, fichier par fichier.                                    |
| [Gestionnaire de feuille de propriétés](propsheet-handlers.md)      | Appelé avant l’affichage de la feuille de propriétés des **Propriétés** d’un objet. Elle vous permet d’ajouter ou de remplacer des pages.                                                              |
| [**Gestionnaire d’images miniatures**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Fournit une image pour représenter l’élément.                                                                                                                                   |
| [**Gestionnaire d'info-bulle**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Fournit du texte contextuel lorsque l’utilisateur place le pointeur de la souris sur l’objet.                                                                                               |
| [**Gestionnaire de métadonnées**](/windows/win32/api/propsys/nn-propsys-ipropertystore)     | Fournit un accès en lecture et en écriture aux métadonnées (propriétés) stockées dans un fichier. Cela peut être utilisé pour étendre le mode Détails, info-bulles, la page de propriétés et les fonctionnalités de regroupement. |



 

Les autres gestionnaires ne sont pas associés à un type de fichier particulier, mais sont appelés avant certaines opérations de Shell :



| Handler                                                            | Description                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestionnaire de colonnes](../lwef/column-handlers.md)                             | appelée par Windows Explorer avant d’afficher la vue détails d’un dossier. Elle vous permet d’ajouter des colonnes personnalisées à la vue Détails.        |
| [Gestionnaire de raccordement de copie](how-to-create-copy-hook-handlers.md)          | Appelé lorsqu’un objet de dossier ou d’imprimante est sur le lieu d’être déplacé, copié, supprimé ou renommé. Elle vous permet d’approuver ou de refuser l’opération.   |
| [Gestionnaire de glisser-déplacer](context-menu-handlers.md)                 | Appelé lorsqu’un fichier est glissé avec le bouton droit de la souris. Elle vous permet de modifier le menu contextuel qui s’affiche.                     |
| [Gestionnaire de superposition d’icône](how-to-implement-icon-overlay-handlers.md) | Appelé avant l’affichage de l’icône d’un fichier. Elle vous permet de spécifier une superposition pour l’icône du fichier.                                          |
| [Gestionnaire de recherche](../lwef/search-handlers.md)                             | Appelé pour lancer un moteur de recherche. elle vous permet d’implémenter un moteur de recherche personnalisé accessible à partir du menu **démarrer** ou de l’explorateur de Windows. |



 

Les détails sur la façon d’implémenter des gestionnaires d’extensions spécifiques sont traités dans les sections répertoriées ci-dessus. Le reste de ce document traite de certains problèmes d’implémentation qui sont communs à tous les gestionnaires d’extensions de Shell.

-   [Implémentation de gestionnaires d’extension de Shell](#implementing-shell-extension-handlers)
    -   [Implémentation de IPersistFile](#implementing-ipersistfile)
    -   [Implémentation de IShellExtInit](#implementing-ishellextinit)
    -   [Personnalisation de l’info-bulle](#infotip-customization)
-   [amélioration de la recherche de Windows avec des gestionnaires d’Extension de Shell](#enhancing-windows-search-with-shell-extension-handlers)
-   [Inscription des gestionnaires d’extensions de Shell](#registering-shell-extension-handlers)
    -   [Noms de gestionnaires](#handler-names)
    -   [Objets Shell prédéfinis](#predefined-shell-objects)
    -   [Exemple d’inscription d’un gestionnaire d’extensions](#example-of-an-extension-handler-registration)
-   [Rubriques connexes](#related-topics)

## <a name="implementing-shell-extension-handlers"></a>Implémentation de gestionnaires d’extension de Shell

La majeure partie de l’implémentation d’un objet de gestionnaire d’extensions de Shell dépend de son type. Toutefois, il existe des éléments communs. Cette section décrit les aspects de l’implémentation qui sont partagés par tous les gestionnaires d’extensions de Shell.

De nombreux gestionnaires d’extension de Shell sont des objets COM (Component Object Model) in-process. Ils doivent recevoir un GUID et être inscrits comme décrit dans inscription des gestionnaires d’extensions de Shell. Elles sont implémentées en tant que dll et doivent exporter les fonctions standard suivantes :

-   [**DllMain**](../dlls/dllmain.md). Point d’entrée standard de la DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Expose la fabrique de classe de l’objet.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM appelle cette fonction pour déterminer si l’objet dessert des clients. Si ce n’est pas le cas, le système peut décharger la DLL et libérer la mémoire associée.

Comme tous les objets COM, les gestionnaires d’extensions de Shell doivent implémenter une interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et une [fabrique de classe](../com/implementing-iclassfactory.md). la plupart des gestionnaires d’extensions doivent également implémenter une interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ou [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) dans Windows XP ou une version antérieure. celles-ci ont été remplacées par [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) et [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) dans Windows Vista. L’interpréteur de commandes utilise ces interfaces pour initialiser le gestionnaire.

L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) doit être implémentée par les éléments suivants :

-   Gestionnaires de données
-   Gestionnaires de suppression

Dans le passé, les gestionnaires d’icônes étaient également requis pour implémenter [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), mais ce n’est plus le cas. Pour les gestionnaires d’icônes, **IPersistFile** est maintenant facultatif et d’autres interfaces telles que [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) sont préférées.

L’interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) doit être implémentée par les éléments suivants :

-   Gestionnaires de menus contextuels
-   Gestionnaires de glisser-déplacer
-   Gestionnaires de feuille de propriétés

### <a name="implementing-ipersistfile"></a>Implémentation de IPersistFile

L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est conçue pour autoriser le chargement d’un objet à partir de ou son enregistrement dans un fichier sur disque. Il a six méthodes en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinq propres et la méthode [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) qu’il hérite de l’interface [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist). Avec les extensions de Shell, **IPersist** est utilisé uniquement pour initialiser un objet de gestionnaire d’extensions de Shell. Étant donné qu’il n’est généralement pas nécessaire de lire ou d’écrire sur le disque, seules les méthodes **GetClassID** et [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) requièrent une implémentation sans jeton.

L’interpréteur de commandes appelle d’abord [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) , et la fonction retourne l’identificateur de classe (CLSID) de l’objet de gestionnaire d’extensions. L’interpréteur de commandes appelle ensuite la [**charge**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) et passe deux valeurs. La première, *pszFileName*, est une chaîne Unicode avec le nom du fichier ou du dossier sur lequel l’interpréteur de commandes va fonctionner. Le deuxième est *dwMode*, qui indique le mode d’accès au fichier. Étant donné qu’il n’est généralement pas nécessaire d’accéder aux fichiers, *dwMode* est généralement égal à zéro. La méthode stocke ces valeurs en fonction des besoins pour une référence ultérieure.

Le fragment de code suivant illustre la façon dont un gestionnaire d’extensions de Shell standard implémente les méthodes [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) et [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) . Il est conçu pour gérer ANSI ou Unicode. CLSID \_ SampleExtHandler est le GUID de l’objet de gestionnaire d’extensions et CSampleExtHandler est le nom de la classe utilisée pour implémenter l’interface. Les variables **m \_ szFileName** et **m \_ dwMode** sont des variables privées utilisées pour stocker le nom et les indicateurs d’accès du fichier.


```C++
wchar_t m_szFileName[MAX_PATH];    // The file name
DWORD m_dwMode;                  // The file access mode

CSampleExtHandler::GetClassID(CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

CSampleExtHandler::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(_szFileName, ARRAYSIZE(m_szFileName), pszFile);
}
```

### <a name="implementing-ishellextinit"></a>Implémentation de IShellExtInit

L’interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) n’a qu’une seule méthode, [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). La méthode a trois paramètres que l’interpréteur de commandes peut utiliser pour passer divers types d’informations. Les valeurs transmises dépendent du type de gestionnaire, tandis que d’autres peuvent avoir la valeur **null**.

-   *pIDFolder* contient le pointeur d’un dossier vers une liste d’identificateurs d’éléments (PIDL). Pour les extensions de feuille de propriétés, la **valeur est null**. Pour les extensions de menu contextuel, il s’agit de l’PIDL du dossier qui contient l’élément dont le menu contextuel est affiché. Pour les gestionnaires de glisser-déplacer non par défaut, il s’agit de l’PIDL du dossier cible.
-   *pDataObject* contient un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) d’un objet de données. L’objet de données contient un ou plusieurs noms de fichiers au format [CF \_ HDROP](dragdrop.md) .
-   *hRegKey* contient une clé de Registre pour l’objet de fichier ou le type de dossier.

La méthode [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) stocke le nom de fichier, le pointeur [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) et la clé de Registre nécessaires pour une utilisation ultérieure. Le fragment de code suivant illustre une implémentation de **IShellExtInit :: Initialize**. Pour plus de simplicité, cet exemple suppose que l’objet de données ne contient qu’un seul fichier. En général, il peut contenir plusieurs fichiers qui devront être extraits.


```C++
LPCITEMIDLIST  m_pIDFolder;           //The folder's PIDL
wchar_t        m_szFile[MAX_PATH];    //The file name
IDataObject   *m_pDataObj;            //The IDataObject pointer
HKEY           m_hRegKey;             //The file or folder's registry key

STDMETHODIMP CShellExt::Initialize(LPCITEMIDLIST pIDFolder, 
                                   IDataObject *pDataObj, 
                                   HKEY hRegKey) 
{ 
    // If Initialize has already been called, release the old PIDL
    ILFree(m_pIDFolder);
    m_pIDFolder = nullptr;

    // Store the new PIDL.
    if (pIDFolder)
    {
        m_pIDFolder = ILClone(pIDFolder);
    }
    
    // If Initialize has already been called, release the old
    // IDataObject pointer.
    if (m_pDataObj)
    { 
        m_pDataObj->Release(); 
    }
     
    // If a data object pointer was passed in, save it and
    // extract the file name. 
    if (pDataObj) 
    { 
        m_pDataObj = pDataObj; 
        pDataObj->AddRef(); 
      
        STGMEDIUM   medium;
        FORMATETC   fe = {CF_HDROP, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};
        UINT        uCount;

        if (SUCCEEDED(m_pDataObj->GetData(&fe, &medium)))
        {
            // Get the count of files dropped.
            uCount = DragQueryFile((HDROP)medium.hGlobal, (UINT)-1, NULL, 0);

            // Get the first file name from the CF_HDROP.
            if (uCount)
                DragQueryFile((HDROP)medium.hGlobal, 0, m_szFile, 
                              sizeof(m_szFile)/sizeof(TCHAR));

            ReleaseStgMedium(&medium);
        }
    }

    // Duplicate the registry handle. 
    if (hRegKey) 
        RegOpenKeyEx(hRegKey, nullptr, 0L, MAXIMUM_ALLOWED, &m_hRegKey); 
    return S_OK; 
}
```

CSampleExtHandler est le nom de la classe utilisée pour implémenter l’interface. Les **variables \_ m pIDFolder**, **m \_ pDataObject**, **m \_ szFileName** et **m \_ hRegKey** sont des variables privées utilisées pour stocker les informations transmises. Par souci de simplicité, cet exemple suppose qu’un seul nom de fichier sera détenu par l’objet de données. Une fois que la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) est Récupérée de l’objet de données, [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) est utilisé pour extraire le nom de fichier du membre **Medium. hGlobal** de la structure **FORMATETC** . Si une clé de Registre est passée, la méthode utilise [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) pour ouvrir la clé et assigne le handle à **m \_ hRegKey**.

### <a name="infotip-customization"></a>Personnalisation de l’info-bulle

Il existe deux façons de personnaliser info-bulles :

-   Implémentez un objet qui prend en charge [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) , puis inscrivez cet objet sous la sous-clé appropriée du Registre (consultez [inscription des gestionnaires d’extensions de Shell](#registering-shell-extension-handlers) ci-dessous).
-   Spécifiez une chaîne fixe ou une liste de propriétés de fichier spécifiques à afficher.

Pour afficher une chaîne fixe pour une extension d’espace de noms, créez une entrée appelée `InfoTip` dans la clé *{CLSID}* de votre extension d’espace de noms. Définissez la valeur de cette entrée de sorte qu’elle soit la chaîne littérale que vous souhaitez afficher, comme illustré dans cet exemple, ou une chaîne indirecte qui spécifie une ressource et un index dans cette ressource (à des fins de localisation).

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Pour afficher une chaîne fixe pour un type de fichier, créez une entrée appelée `InfoTip` dans la clé *ProgID* de ce type de fichier. Définissez la valeur de cette entrée sur la chaîne littérale que vous souhaitez afficher ou sur une chaîne indirecte qui spécifie une ressource et un index au sein de cette ressource (à des fins de localisation), comme illustré dans cet exemple.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = Resource.dll, 3
```

Si vous souhaitez que l’interpréteur de commandes affiche des propriétés de fichier spécifiques dans l’info-bulle pour un type de fichier spécifique, créez une entrée appelée `InfoTip` dans la clé *ProgID* pour ce type de fichier. Définissez la valeur de cette entrée sur une liste délimitée par des points-virgules de noms de propriétés canoniques, d’identificateurs de format (FMTID) de paires d’identificateurs (PID)/Property, ou les deux. Cette valeur doit commencer par « prop : » pour l’identifier en tant que chaîne de liste de propriétés. Si vous omettez « prop : », la valeur est considérée comme une chaîne littérale et affichée comme telle.

Dans l’exemple suivant, *propName* est un nom de propriété canonique (tel que System. date) et *{fmtid}, PID* est une paire [**fmtid/PID**](./objects.md) .

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = prop:propname;propname;{fmtid},pid;{fmtid},pid
```

Les noms de propriétés suivants peuvent être utilisés :



| Nom de la propriété    | Description                   | Récupéré à partir de                                                                             |
|------------------|-------------------------------|--------------------------------------------------------------------------------------------|
| Auteur           | Auteur du document        | [**\_auteur PIDSI**](../stg/the-summary-information-property-set.md)                              |
| Intitulé            | Titre du document         | [**\_titre PIDSI**](../stg/the-summary-information-property-set.md)                               |
| Objet          | Résumé de l’objet               | [**PIDSI \_ objet**](../stg/the-summary-information-property-set.md)                             |
| Commentaire          | Commentaires sur le document             | [**PIDSI \_**](../stg/the-summary-information-property-set.md) Propriétés d’un commentaire ou d’un dossier/pilote |
| PageCount        | Nombre de pages               | [**PIDSI \_ PageCount**](../stg/the-summary-information-property-set.md)                           |
| Nom             | Nom convivial                 | Affichage des dossiers standard                                                                       |
| OriginalLocation | Emplacement du fichier d’origine     | Dossier porte-documents et dossier Corbeille                                                    |
| DateDeleted      | Date de suppression du fichier         | Dossier Corbeille                                                                         |
| Type             | Type de fichier                  | Mode Détails du dossier standard                                                               |
| Taille             | Taille du fichier                  | Mode Détails du dossier standard                                                               |
| SyncCopyIn       | Identique à OriginalLocation      | Identique à OriginalLocation                                                                   |
| Modifié le         | Date de dernière modification            | Mode Détails du dossier standard                                                               |
| Date de création          | Date de création                  | Mode Détails du dossier standard                                                               |
| Atteint         | Date du dernier accès            | Mode Détails du dossier standard                                                               |
| Indossier         | Répertoire contenant le fichier | Résultats de la recherche de documents                                                                    |
| Rank             | Qualité de la recherche de correspondance       | Résultats de la recherche de documents                                                                    |
| FreeSpace        | Espace de stockage disponible       | Lecteurs de disque                                                                                |
| NumberOfVisits   | Nombre de visites              | Dossier Favoris                                                                           |
| Attributs       | Attributs de fichier               | Mode Détails du dossier standard                                                               |
| Company          | Nom de la société                  | [**\_entreprise PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)    |
| Category         | Catégorie de document             | [**\_catégorie PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| copyright        | Copyright du support               | [**\_Copyright PIDMSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| HTMLInfoTipFile  | Fichier info-bulle HTML             | Fichier Desktop.ini pour le dossier                                                                |



 

## <a name="enhancing-windows-search-with-shell-extension-handlers"></a>amélioration de la recherche de Windows avec des gestionnaires d’Extension de Shell

les gestionnaires d’extensions de Shell peuvent être utilisés pour améliorer l’expérience utilisateur fournie par un gestionnaire de protocole de recherche Windows. Pour activer ces améliorations, le gestionnaire d’extensions de Shell de prise en charge doit être conçu pour s’intégrer au gestionnaire de protocole de recherche comme source de données. pour plus d’informations sur la façon d’améliorer un gestionnaire de protocole de recherche de Windows par le biais de l’intégration à un gestionnaire d’extensions de Shell, consultez [ajout d’icônes, d’aperçus et de Menus contextuels](../search/-search-3x-wds-ph-ui-extensions.md). pour plus d’informations sur les gestionnaires de protocoles de recherche Windows, consultez [développement de gestionnaires de protocole](../search/-search-3x-wds-phaddins.md).

## <a name="registering-shell-extension-handlers"></a>Inscription des gestionnaires d’extensions de Shell

Un objet de gestionnaire d’extensions d’interpréteur de commandes doit être inscrit pour que l’interpréteur de commandes puisse l’utiliser. Cette section est une discussion générale sur l’enregistrement d’un gestionnaire d’extensions de Shell.

Chaque fois que vous créez ou modifiez un gestionnaire d’extensions de Shell, il est important d’informer le système que vous avez apporté une modification à [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), en spécifiant l’événement **\_ ASSOCCHANGED SHCNE** . Si vous n’appelez pas **SHChangeNotify**, la modification peut ne pas être reconnue tant que le système n’est pas redémarré.

Comme avec tous les objets COM, vous devez créer un GUID pour le gestionnaire à l’aide d’un outil tel que UUIDGEN.exe. Créez une clé sous le CLSID **\_ \_ racine des classes HKEY** dont le \\  nom est le format de chaîne du GUID. Étant donné que les gestionnaires d’extensions de Shell sont des serveurs in-process, vous devez créer une clé **InprocServer32** sous la clé GUID avec la valeur par défaut définie sur le chemin d’accès de la dll du gestionnaire. Utilisez le modèle de thread cloisonné.

Chaque fois que l’interpréteur de commandes prend une mesure qui peut impliquer un gestionnaire d’extensions de Shell, il vérifie la clé de registre appropriée. La clé sous laquelle un gestionnaire d’extensions est inscrit, contrôle le moment où il sera appelé. Par exemple, il est courant d’avoir un gestionnaire de menu contextuel appelé lorsque l’interpréteur de commandes affiche un menu contextuel pour un membre d’un [type de fichier](fa-file-types.md). Dans ce cas, le gestionnaire doit être inscrit sous la clé **ProgID** du type de fichier.

### <a name="handler-names"></a>Noms de gestionnaires

Pour activer un gestionnaire d’extensions de Shell, créez une sous-clé avec le nom de la sous-clé du gestionnaire (voir ci-dessous) sous la sous-clé **shellex** du **ProgID** (pour les types de fichiers) ou du nom du type d’objet Shell (pour les [objets Shell prédéfinis](#predefined-shell-objects)).

Par exemple, si vous souhaitez inscrire un gestionnaire d’extension de menu contextuel pour MyProgram. 1, vous devez commencer par créer la sous-clé suivante :

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Pour les gestionnaires suivants, créez une sous-clé sous la clé « nom de la sous-clé du gestionnaire » dont le nom est la version de chaîne du CLSID de l’extension de Shell. Plusieurs extensions peuvent être inscrites sous la clé de nom de la sous-clé du gestionnaire en créant plusieurs sous-clés.



| Handler                                               | Interface          | Nom de la sous-clé du gestionnaire       |
|-------------------------------------------------------|--------------------|---------------------------|
| Gestionnaire de menu contextuel                                 | IContextMenu       | **ContextMenuHandlers**   |
| Gestionnaire CopyHook                                      | ICopyHook          | **CopyHookHandlers**      |
| Gestionnaire de glisser-déplacer                                 | IContextMenu       | **DragDropHandlers**      |
| Gestionnaire de feuille de propriétés                                | IShellPropSheetExt | **PropertySheetHandlers** |
| gestionnaire de fournisseur de colonne (déconseillé dans Windows Vista) | IColumnProvider    | **ColumnHandlers**        |



 

Pour les gestionnaires suivants, la valeur par défaut de la clé « nom de la sous-clé du gestionnaire » est la version de chaîne du CLSID de l’extension de Shell. Une seule extension peut être inscrite pour ces gestionnaires.



| Handler                 | Interface                                         | Nom de la sous-clé du gestionnaire                        |
|-------------------------|---------------------------------------------------|--------------------------------------------|
| Gestionnaire de données            | IDataObject                                       | **DataHandler**                            |
| Supprimer le gestionnaire            | IDropTarget                                       | **DropHandler**                            |
| Gestionnaire d’icône            | IExtractIconA/W                                   | **IconHandler**                            |
| Gestionnaire d’images           | IExtractImage                                     | **{BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}** |
| Gestionnaire d’images miniatures | IThumbnailProvider                                | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Gestionnaire d'info-bulle         | IQueryInfo                                        | **{00021500-0000-0000-C000-000000000046}** |
| Lien de Shell (ANSI)      | IShellLinkA                                       | **{000214EE-0000-0000-C000-000000000046}** |
| Lien de Shell (UNICODE)    | IShellLinkW                                       | **{000214F9-0000-0000-C000-000000000046}** |
| Stockage structuré      | IStorage                                          | **{0000000B-0000-0000-C000-000000000046}** |
| Métadonnées                | IPropertyStore                                    | **PropertyHandler**                        |
| Métadonnées                | IPropertySetStorage (déconseillé dans Windows Vista) | **PropertyHandler**                        |
| Épingler au menu Démarrer       | IStartMenuPinnedList                              | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Épingler à la barre des tâches          |                                                   | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Les sous-clés spécifiées pour ajouter **Épingler au menu Démarrer** et **Épingler à la barre des tâches** dans le menu contextuel d’un élément ne sont nécessaires que pour les types de fichiers qui incluent l’entrée [IsShortCut](./links.md) .

la prise en charge des gestionnaires de fournisseur de colonne a été supprimée dans Windows Vista. en outre, à partir de Windows Vista, [**IPropertySetStorage**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) a été déconseillé en faveur de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

bien que [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) reste pris en charge, [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) est préférable pour Windows Vista et versions ultérieures.

### <a name="predefined-shell-objects"></a>Objets Shell prédéfinis

L’interpréteur de commandes définit des objets supplémentaires sous la **\_ \_ racine HKEY classes** qui peuvent être étendus de la même façon que les types de fichiers. Par exemple, pour ajouter un gestionnaire de feuille de propriétés pour tous les fichiers, vous pouvez vous inscrire sous la clé **PropertySheetHandlers** .

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

Le tableau suivant indique les différentes sous-clés de la **\_ \_ racine de la classe HKEY** sous lesquelles les gestionnaires d’extension peuvent être inscrits. Notez que de nombreux gestionnaires d’extension ne peuvent pas être enregistrés sous toutes les sous-clés répertoriées. Pour plus d’informations, consultez la documentation du gestionnaire spécifique.



| Sous-clé                    | Description                                                          | Gestionnaires possibles                                | Version |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|---------|
| **\***                    | Tous les fichiers                                                            | Menu contextuel, feuille de propriétés, verbes (voir ci-dessous) | Tous     |
| **AllFileSystemObjects**  | Tous les fichiers et dossiers de fichiers                                           | Menu contextuel, feuille de propriétés, verbes             | 4.71    |
| **Folder**                | Tous les dossiers                                                          | Menu contextuel, feuille de propriétés, verbes             | Tous     |
| **Directory**             | Dossiers de fichiers                                                         | Menu contextuel, feuille de propriétés, verbes             | Tous     |
| **\\Arrière-plan du répertoire** | Arrière-plan du dossier de fichiers                                               | Menu contextuel uniquement                               | 4.71    |
| **Lecteur**                 | Tous les lecteurs dans MyComputer, tels que « C : \\ »                             | Menu contextuel, feuille de propriétés, verbes             | Tous     |
| **Réseau**               | Tout le réseau (sous Favoris réseau)                             | Menu contextuel, feuille de propriétés, verbes             | Tous     |
| **Type de réseau \\\\\#**     | Tous les objets de type \# (voir ci-dessous)                                   | Menu contextuel, feuille de propriétés, verbes             | 4.71    |
| **NetShare**              | Tous les partages réseau                                                   | Menu contextuel, feuille de propriétés, verbes             | 4.71    |
| **Serveur netserver**             | Tous les serveurs réseau                                                  | Menu contextuel, feuille de propriétés, verbes             | 4.71    |
| *\_nom du fournisseur réseau \_* | Tous les objets fournis par le fournisseur réseau «*\_ \_ nom du fournisseur réseau*» | Menu contextuel, feuille de propriétés, verbes             | Tous     |
| **Imprimantes**              | Toutes les imprimantes                                                         | Menu contextuel, feuille de propriétés                    | Tous     |
| **AudioCD**               | CD audio dans le lecteur CD                                                 | Verbes uniquement                                       | Tous     |
| **DVD**                   | lecteur de DVD (Windows 2000)                                             | Menu contextuel, feuille de propriétés, verbes             | 4.71    |



 

Remarques :

-   Le menu contextuel de l’arrière-plan du dossier de fichiers est accessible en cliquant avec le bouton droit dans un dossier de fichiers, mais pas sur le contenu du dossier.
-   Les « verbes » sont des commandes spéciales **inscrites sous le \_ \_** verbe de Shell de la \\ *sous-clé* de l' \\ **interpréteur** de commandes \\  .
-   Pour le type de **réseau** \\  \\ **\#** , « \# » est un code de type de fournisseur réseau au format décimal. Le code du type de fournisseur réseau est le mot de poids fort d’un type de réseau. La liste des types de réseau est fournie dans le fichier d’en-tête Winnetwk. h ( \_ valeurs net WNNC \_ \* ). Par exemple, WNNC \_ NET \_ Shiva est 0x00330000. par conséquent, la clé de type correspondante serait de type HKEY de la **\_ \_ racine** de \\  \\ **type** \\ **51** .
-   «*\_ \_ nom du fournisseur réseau*» est un nom de fournisseur réseau spécifié par [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), avec les espaces convertis en traits de soulignement. par exemple, si le fournisseur réseau de réseau microsoft est installé, son nom de fournisseur est « microsoft Windows network » et le *\_ \_ nom du fournisseur réseau* correspondant est **Microsoft \_ Windows \_ réseau**.

### <a name="example-of-an-extension-handler-registration"></a>Exemple d’inscription d’un gestionnaire d’extensions

Pour activer un gestionnaire spécifique, créez une sous-clé sous la clé de type de gestionnaire d’extension avec le nom du gestionnaire. L’interpréteur de commandes n’utilise pas le nom du gestionnaire, mais il doit être différent de tous les autres noms sous cette sous-clé de type. Définissez la valeur par défaut de la sous-clé Name sur la forme de chaîne du GUID du gestionnaire.

L’exemple suivant illustre les entrées de Registre qui activent les gestionnaires d’extensions de menu contextuel et de feuille de propriétés, à l’aide d’un exemple de type de fichier. MYP :

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

la procédure d’inscription décrite dans cette section doit être suivie pour tous les systèmes de Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conseils pour l’implémentation des extensions de In-Process](shell-and-managed-code.md)
</dt> </dl>

 

 
