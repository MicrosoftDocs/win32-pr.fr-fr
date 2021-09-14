---
description: La procédure d’implémentation d’une extension d’espace de noms est semblable à celle de tout autre objet COM (Component Object Model) in-process.
title: Implémentation des interfaces d’objets de dossier de base
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a45b8011-5355-429b-8935-4a7bdb5d2316
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05f5d2e4c21a923856c7324ad2d407230fa7595
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235206"
---
# <a name="implementing-the-basic-folder-object-interfaces"></a>Implémentation des interfaces d’objets de dossier de base

La procédure d’implémentation d’une extension d’espace de noms est semblable à celle de tout autre objet COM (Component Object Model) in-process. toutes les extensions doivent prendre en charge trois interfaces principales qui fournissent à Windows Explorer les informations de base nécessaires à l’affichage des dossiers de l’extension dans l’arborescence. toutefois, pour tirer pleinement parti des fonctionnalités de Windows Explorer, votre extension doit également exposer une ou plusieurs interfaces facultatives qui prennent en charge des fonctionnalités plus sophistiquées, telles que des menus contextuels ou des opérations de glisser-déplacer, et fournissent un affichage des dossiers.

ce document explique comment implémenter les interfaces principales et facultatives que Windows Explorer appelle pour obtenir des informations sur le contenu de votre extension. pour plus d’informations sur l’implémentation d’un affichage des dossiers et sur la personnalisation de l’explorateur de Windows, consultez [implémentation d’un affichage des dossiers](../lwef/nse-folderview.md).

-   [Implémentation et inscription de base](#basic-implementation-and-registration)
    -   [Inscription d’une extension](#registering-an-extension)
-   [Gestion de PIDL](#handling-pidls)
    -   [Création d’une structure SHITEMID](#creating-an-shitemid-structure)
    -   [Construction d’un PIDL](#constructing-a-pidl)
    -   [Interprétation des PIDL](#interpreting-pidls)
-   [Implémentation des interfaces principales](#implementing-the-primary-interfaces)
    -   [Interface IPersistFolder](#ipersistfolder-interface)
    -   [Interface IShellFolder](#ishellfolder-interface)
    -   [Interface IEnumIDList](#ienumidlist-interface)
-   [Implémentation des interfaces facultatives](#implementing-the-optional-interfaces)
    -   [IExtractIcon](#iextracticon)
    -   [IContextMenu](#icontextmenu)
    -   [IQueryInfo](#iqueryinfo)
    -   [IDataObject et IDropTarget](#idataobject-and-idroptarget)
-   [Utilisation de l’implémentation de l’affichage des dossiers shell par défaut](#working-with-the-default-shell-folder-view-implementation)

## <a name="basic-implementation-and-registration"></a>Implémentation et inscription de base

En tant que serveur COM in-process, votre DLL doit exposer plusieurs fonctions et interfaces standard :

-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)
-   [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Ces fonctions et interfaces sont implémentées de la même façon que pour la plupart des autres objets COM. Pour plus d’informations, consultez la [documentation com](../com/the-component-object-model.md).

### <a name="registering-an-extension"></a>Inscription d’une extension

Comme pour tous les objets COM, vous devez créer un GUID de l’identificateur de classe (CLSID) pour votre extension. Inscrivez l’objet en créant une sous-clé du CLSID **\_ \_ racine de la classe HKEY** \\  nommée pour le CLSID de votre extension. La DLL doit être inscrite en tant que serveur in-process et doit spécifier le modèle de thread cloisonné. Vous pouvez personnaliser le comportement du dossier racine d’une extension en ajoutant une série de sous-clés et de valeurs à la clé CLSID de l’extension.

Plusieurs de ces valeurs s’appliquent uniquement aux extensions avec des points de jonction virtuels. Ces valeurs ne s’appliquent pas aux extensions dont les points de jonction sont des dossiers du système de fichiers. Pour plus d’informations, consultez [spécification de l’emplacement d’une extension d’espace de noms](nse-junction.md). Pour modifier le comportement d’une extension avec un point de jonction virtuel, ajoutez une ou plusieurs des valeurs suivantes à la clé CLSID de l’extension :

-   WantsFORPARSING. Le nom d’analyse d’une extension avec un point de jonction virtuel aura normalement la forme :: {*GUID*}. Les extensions de ce type contiennent normalement des éléments virtuels. Toutefois, certaines extensions, telles que mes documents, correspondent en fait à des dossiers du système de fichiers, même si elles ont des points de jonction virtuels. Si votre extension représente des objets de système de fichiers de cette façon, vous pouvez définir la valeur WantsFORPARSING. Windows L’Explorateur demande ensuite le nom d’analyse de votre dossier racine en appelant la méthode [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) de l’objet Folder avec *UFlags* défini sur **SHGDN \_ FORPARSING** et *PIDL* défini sur un pointeur vide unique vers une liste d’identificateurs d’éléments (PIDL). Un PIDL vide contient uniquement un terminateur. Votre méthode doit ensuite retourner le nom de l’analyse du dossier racine :: {*GUID*}.
-   HideFolderVerbs. Les verbes inscrits sous le dossier **\_ \_ racine de la classe HKEY** \\  sont normalement associés à toutes les extensions. Elles s’affichent dans le menu contextuel de l’extension et peuvent être appelées par [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea). Pour empêcher l’Association de ces verbes à votre extension, définissez la valeur HideFolderVerbs.
-   HideAsDelete. si un utilisateur tente de supprimer votre extension, Windows Explorer masquera l’extension.
-   HideAsDeletePerUser. Cette valeur a le même effet que HideAsDelete, mais pour chaque utilisateur. L’extension est masquée uniquement pour les utilisateurs qui ont tenté de la supprimer. L’extension est visible par tous les autres utilisateurs.
-   QueryForOverlay. Définissez cette valeur pour indiquer que l’icône du dossier racine peut avoir une icône de superposition. L’objet Folder doit prendre en charge l’interface [**IShellIconOverlay**](/windows/win32/api/shlobj_core/nn-shlobj_core-ishelliconoverlay) . avant que Windows Explorer n’affiche l’icône du dossier racine, il demande une icône de recouvrement en appelant l’une des deux méthodes **IShellIconOverlay** avec *pidlItem* défini sur un PIDL vide.

Les valeurs restantes et les sous-clés s’appliquent à toutes les extensions :

-   Pour spécifier le nom d’affichage du dossier du point de jonction de l’extension, définissez la valeur par défaut de la sous-clé CLSID de l’extension sur une chaîne appropriée.
-   Quand le curseur pointe sur un dossier, une info-bulle s’affiche généralement pour décrire le contenu du dossier. Pour fournir une info-bulle pour le dossier racine de votre extension, créez une valeur de **Registre \_** de l’info-bulle pour la clé CLSID de l’extension et affectez-lui une chaîne appropriée.
-   Pour spécifier une icône personnalisée pour le dossier racine de votre extension, créez une sous-clé de la sous-clé CLSID de l’extension nommée **DefaultIcon**. Définissez la valeur par défaut de **DefaultIcon** sur une valeur **reg \_ SZ** contenant le nom du fichier qui contient l’icône, suivi d’une virgule, suivi d’un signe moins, suivi de l’index de l’icône dans ce fichier.
-   Par défaut, le menu contextuel du dossier racine de votre extension contient les éléments définis sous **le \_ \_ \\ dossier racine** de la section HKEY classes. Les éléments **supprimer**, **Renommer** et **Propriétés** sont ajoutés si vous avez défini les \_ indicateurs SFGAO xxx appropriés. Vous pouvez ajouter d’autres éléments dans le menu contextuel du dossier racine ou remplacer les éléments existants, comme vous le feriez pour un [type de fichier](fa-file-types.md). Créez une sous-clé **Shell** sous la clé CLSID de l’extension et définissez les commandes comme indiqué dans [extension des menus contextuels](context.md).
-   Si vous avez besoin d’une méthode plus flexible pour gérer le menu contextuel du dossier racine, vous pouvez implémenter un [Gestionnaire de menu contextuel](context-menu-handlers.md). Pour inscrire le gestionnaire de menu contextuel, créez une clé **shellex** sous la clé CLSID de l’extension. Enregistrez le CLSID du gestionnaire comme vous le feriez pour un gestionnaire d' [extension de Shell de création](handlers.md)conventionnel.
-   Pour ajouter une page à la feuille de propriétés propriétés du dossier racine, attribuez le dossier à l’attribut **SFGAO \_ HASPROPSHEET** et implémentez un [Gestionnaire de feuille de propriétés](propsheet-handlers.md). Pour inscrire le gestionnaire de la feuille de propriétés, créez une clé **shellex** sous la clé CLSID de l’extension. Enregistrez le CLSID du gestionnaire comme vous le feriez pour un gestionnaire d' [extension de Shell de création](handlers.md)conventionnel.
-   Pour spécifier les attributs du dossier racine, ajoutez une sous-clé **ShellFolder** à la sous-clé CLSID de l’extension. Créez une valeur d’attributs et affectez-lui la combinaison appropriée d’indicateurs [**SFGAO \_ xxx**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) .

Le tableau suivant répertorie certains attributs couramment utilisés pour les dossiers racine.



| Indicateur                | Valeur      | Description                                                                                                                                                                                                                                                                                                       |
|---------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_dossier SFGAO       | 0x20000000 | Le dossier racine de l’extension contient un ou plusieurs éléments.                                                                                                                                                                                                                                                           |
| SFGAO \_ HASSUBFOLDER | 0x80000000 | Le dossier racine de l’extension contient un ou plusieurs sous-dossiers. Windows L’Explorateur place un signe plus (+) en regard de l’icône de dossier.                                                                                                                                                                               |
| SFGAO \_ CANDELETE    | 0x00000020 | Le dossier racine de l’extension peut être supprimé par l’utilisateur. Le menu contextuel du dossier comportera un élément **supprimer** . Cet indicateur doit être défini pour les points de jonction placés sous l’un des [dossiers virtuels](nse-junction.md).                                                                                 |
| SFGAO \_ CANRENAME    | 0x00000010 | Le dossier racine de l’extension peut être renommé par l’utilisateur. Le menu contextuel du dossier aura un élément **Renommer** .                                                                                                                                                                                                   |
| SFGAO \_ HASPROPSHEET | 0x00000040 | Le dossier racine de l’extension contient une feuille de propriétés **Propriétés** . Le menu contextuel du dossier comporte un élément **Propriétés** . Pour fournir la feuille de propriétés, vous devez implémenter un [Gestionnaire de feuille de propriétés](propsheet-handlers.md). Inscrivez le gestionnaire sous la clé CLSID de l’extension, comme indiqué précédemment. |



 

L’exemple suivant illustre l’entrée de Registre CLSID pour une extension avec un nom d’affichage MyExtension. L’extension a une icône personnalisée qui est contenue dans la DLL de l’extension avec un index de 1. Les **attributs \_ SFGAO**, **SFGAO \_ HASSUBFOLDER** et **SFGAO \_ CANDELETE** sont définis.

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         (Default) = MyExtension
         InfoTip = Some appropriate text
      DefaultIcon
         (Default) = c:\MyDir\MyExtension.dll,-1
      InProcServer32
         (Default) = c:\MyDir\MyExtension.dll
         ThreadingModel = Apartment
      ShellFolder
         Attributes = 0xA00000020
```

## <a name="handling-pidls"></a>Gestion de PIDL

Chaque élément de l’espace de noms Shell doit avoir un PIDL unique. Windows L’Explorateur assigne un PIDL à votre dossier racine et passe la valeur à votre extension pendant l’initialisation. votre extension est alors chargée d’attribuer un PIDL correctement construit à chacun de ses objets et de fournir ces pidl à Windows Explorer à la demande. Lorsque l’interpréteur de commandes utilise un PIDL pour identifier l’un des objets de votre extension, votre extension doit être en mesure d’interpréter le PIDL et d’identifier l’objet particulier. Votre extension doit également assigner un [**nom complet**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof) et un *nom d’analyse* à chaque objet. Étant donné que les PIDL sont utilisés par pratiquement toutes les interfaces de dossiers, les extensions implémentent généralement un *Gestionnaire PIDL* unique pour gérer toutes ces tâches.

Le terme PIDL est concis pour une structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) ou un pointeur vers une telle structure, selon le contexte. Comme déclaré, une structure **ITEMIDLIST** a un seul membre, une structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . La structure **ITEMIDLIST** d’un objet est en fait un tableau condensé de deux structures **SHITEMID** ou plus. L’ordre de ces structures définit un chemin d’accès à l’aide de l’espace de noms, à peu près de la même façon que c : \\ mydirectory \\ MyFile définit un chemin d’accès via le système de fichiers. En règle générale, le PIDL d’un objet se compose d’une série de structures **SHITEMID** qui correspondent aux dossiers qui définissent le chemin d’accès de l’espace de noms, suivis de la structure **SHITEMID** de l’objet, suivie d’un terminateur.

Le terminateur est une structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , avec le membre *CB* ayant la valeur **null**. Le terminateur est nécessaire car le nombre de structures **SHITEMID** dans le PIDL d’un objet dépend de l’emplacement de l’objet dans l’espace de noms de l’interpréteur de commandes et du point de départ du chemin d’accès. En outre, la taille des différentes structures **SHITEMID** peut varier. Quand vous recevez un PIDL, vous n’avez aucun moyen simple de déterminer sa taille, voire le nombre total de structures **SHITEMID** . Au lieu de cela, vous devez « parcourir » le tableau condensé, structure par structure, jusqu’à ce que vous atteigniez le terminateur.

Pour créer un PIDL, votre application doit :

1.  Créez une structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) pour chacun de ses objets.
2.  Assemblez les structures [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) pertinentes dans un PIDL.

### <a name="creating-an-shitemid-structure"></a>Création d’une structure SHITEMID

La structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) d’un objet identifie l’objet de manière unique dans son dossier. En fait, un type de PIDL utilisé par la plupart des méthodes [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) se compose uniquement de la structure **SHITEMID** de l’objet, suivie d’un terminateur. La définition d’une structure **SHITEMID** est la suivante :


```C++
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



Le membre *abID* est l’identificateur de l’objet. Étant donné que la longueur de *abID* n’est pas définie et peut varier, le membre *CB* est défini sur la taille de la structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , en octets.

Étant donné que la longueur et le contenu de *abID* ne sont pas normalisés, vous pouvez utiliser n’importe quel schéma pour assigner des valeurs *abID* à vos objets. La seule exigence est que vous ne pouvez pas avoir deux objets dans le même dossier avec des valeurs identiques. Toutefois, pour des raisons de performances, votre structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) doit être alignée sur les **DWORD**. En d’autres termes, vous devez construire vos valeurs *abID* de sorte que *CB* soit un multiple entier de 4.

En général, *abID* pointe vers une structure définie par l’extension. En plus de l’ID de l’objet, cette structure est souvent utilisée pour contenir diverses informations connexes, telles que le type ou les attributs de l’objet. Les objets de dossier de votre extension peuvent ensuite extraire rapidement les informations du PIDL au lieu de devoir les interroger.

> [!Note]  
> L’un des aspects les plus importants de la conception d’une structure de données pour un PIDL est de rendre la structure persistante et transportable. Dans le contexte de PIDL, la signification de ces termes est la suivante :
>
> -   Persistant. Le système place souvent PIDL dans différents types de stockage à long terme, tels que des fichiers de raccourcis. Il peut ensuite récupérer ces PIDL à partir du stockage ultérieurement, éventuellement après le redémarrage du système. Un PIDL récupéré à partir du stockage doit toujours être valide et explicite pour votre extension. Cette exigence signifie, par exemple, que vous ne devez pas utiliser de pointeurs ou de handles dans votre structure PIDL. Les PIDL contenant ce type de données ne sont normalement pas sensées lorsque le système les récupère ultérieurement à partir du stockage.
> -   Transportables. Un PIDL doit rester explicite lorsqu’il est transporté d’un ordinateur à un autre. Par exemple, un PIDL peut être écrit dans un fichier de raccourci, copié sur une disquette et transporté vers un autre ordinateur. Cette PIDL doit toujours être significative pour votre extension s’exécutant sur le deuxième ordinateur. Par exemple, pour vous assurer que vos PIDL sont transportables, utilisez explicitement des caractères ANSI ou Unicode. Évitez les types de données tels que **TCHAR** ou **LPTStr**. Si vous utilisez ces types de données, un PIDL créé sur un ordinateur exécutant une version Unicode de votre extension ne sera pas lisible par une version ANSI de cette extension s’exécutant sur un autre ordinateur.

 

La déclaration suivante montre un exemple simple d’une structure de données.


```C++
typedef struct tagMYPIDLDATA {
  USHORT cb;
  DWORD dwType;
  WCHAR wszDisplayName[40];
} MYPIDLDATA, *LPMYPIDLDATA;
```



Le membre **CB** est défini sur la taille de la structure **MYPIDLDATA** . Ce membre fait de **MYPIDLDATA** une structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) valide, dans et de lui-même. Les autres membres sont équivalents au membre **abID** d’une structure **SHITEMID** et contiennent des données privées. Le membre **dwType** est une valeur définie par une extension qui indique le type d’objet. Pour cet exemple, **dwType** est défini sur **true** pour les dossiers et **false** dans le cas contraire. Ce membre vous permet, par exemple, de déterminer rapidement si l’objet est un dossier ou non. Le membre **wszDisplayName** contient le nom complet de l’objet. Étant donné que vous n’affectez pas le même nom d’affichage à deux objets différents dans le même dossier, le nom complet sert également d’ID d’objet. Dans cet exemple, **wszDisplayName** est défini sur 40 caractères pour garantir que la structure **SHITEMID** sera alignée sur la valeur **DWORD**. Pour limiter la taille de votre PIDL, vous pouvez utiliser à la place un tableau de caractères de longueur variable et ajuster la valeur de CB en conséquence. Remplissez la chaîne d’affichage avec suffisamment de \\ caractères « 0 » pour conserver l’alignement **DWORD** de la structure. Les autres membres qui peuvent être utiles pour la mise en place de la structure incluent la taille, les attributs ou le nom de l’analyse de l’objet.

### <a name="constructing-a-pidl"></a>Construction d’un PIDL

Une fois que vous avez défini les structures [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) pour vos objets, vous pouvez les utiliser pour construire un PIDL. Les PIDL peuvent être construits à diverses fins, mais la plupart des tâches utilisent l’un des deux types de PIDL. Le plus simple, un PIDL à un seul niveau, identifie l’objet par rapport à son dossier parent. Ce type de PIDL est utilisé par la plupart des méthodes [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Un PIDL à un seul niveau contient la structure **SHITEMID** de l’objet, suivie d’un terminateur. Un PIDL qualifié complet définit un chemin d’accès via la hiérarchie d’espaces de noms à partir du bureau vers l’objet. Ce type de PIDL démarre sur le bureau et contient une structure **SHITEMID** pour chaque dossier du chemin d’accès, suivi de l’objet et du terminateur. Un PIDL complet identifie de façon unique l’objet dans l’intégralité de l’espace de noms de l’interpréteur de commandes.

La façon la plus simple de construire un PIDL consiste à travailler directement avec la structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) elle-même. Créez une structure **ITEMIDLIST** , mais allouez suffisamment de mémoire pour contenir toutes les structures [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . L’adresse de cette structure pointera vers la structure **SHITEMID** initiale. Définissez les valeurs des membres de cette structure initiale, puis ajoutez autant de structures **SHITEMID** supplémentaires que nécessaire, dans l’ordre approprié. La procédure suivante décrit comment créer un PIDL à un seul niveau. Il contient deux structures **SHITEMID** , une structure **MYPIDLDATA** suivie d’un terminateur :

1.  Utilisez la fonction [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer de la mémoire pour le PIDL. Allouez suffisamment de mémoire pour vos données privées plus un **UShort** (deux octets) pour le terminateur. Effectuez un cast du résultat en LPMYPIDLDATA.
2.  Définissez le membre CB de la première structure **MYPIDLDATA** sur la taille de cette structure. Pour cet exemple, vous devez affecter à **CB** la valeur sizeof (MYPIDLDATA). Si vous souhaitez utiliser une structure de longueur variable, vous devez calculer la valeur de **CB**.
3.  Assignez des valeurs appropriées aux membres de données privés.
4.  Calcule l’adresse de la structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) suivante. Effectuez un cast de l’adresse de la structure MYPIDLDATA actuelle en LPBYTE, puis ajoutez cette valeur à la valeur de **CB** déterminée à l’étape 3.
5.  Dans ce cas, la prochaine structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) est le terminateur. Affectez la valeur zéro au membre **CB** de la structure.

Pour les PIDL plus longues, allouez suffisamment de mémoire et répétez les étapes 3-5 pour chaque structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) supplémentaire.

L’exemple de fonction suivant prend le type et le nom d’affichage d’un objet et retourne le PIDL à un seul niveau de l’objet. La fonction suppose que le nom d’affichage, y compris son caractère **null** de fin, ne dépasse pas le nombre de caractères déclarés pour la structure **MYPIDLDATA** . Si cette supposition s’avère incorrecte, la fonction [**StringCbCopyW**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) tronque le nom complet. La variable **g \_ pMalloc** est un pointeur [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) créé ailleurs et stocké dans une variable globale.


```C++
LPITEMIDLIST CreatePIDL(DWORD dwType, LPCWSTR pwszDisplayName)
{
    LPMYPIDLDATA   pidlOut;
    USHORT         uSize;

    pidlOut = NULL;

    //Calculate the size of the MYPIDLDATA structure.
    uSize = sizeof(MYPIDLDATA);

    // Allocate enough memory for the PIDL to hold a MYPIDLDATA structure 
    // plus the terminator
    pidlOut = (LPMYPIDLDATA)m_pMalloc->Alloc(uSize + sizeof(USHORT));

    if(pidlOut)
    {
       //Assign values to the members of the MYPIDLDATA structure
       //that is the PIDL's first SHITEMID structure
       pidlOut->cb = uSize;
       pidlOut->dwType = dwType;
       hr = StringCbCopyW(pidlOut->wszDisplayName, 
                          sizeof(pidlOut->wszDisplayName), pwszDisplayName);
       
       // TODO: Add error handling here to verify the HRESULT returned 
       // by StringCbCopyW.

       //Advance the pointer to the start of the next SHITEMID structure.
       pidlOut = (LPMYPIDLDATA)((LPBYTE)pidlOut + pidlOut->cb);

       //Create the terminating null character by setting cb to 0.
       pidlOut->cb = 0;
    }

    return pidlOut;
```



Un PIDL complet doit avoir des structures [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) pour chaque objet du bureau vers votre objet. Votre extension reçoit un PIDL complet pour votre dossier racine lorsque l’interpréteur de commandes appelle [**IPersistFolder :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize). Pour construire un PIDL qualifié complet pour un objet, prenez le PIDL que l’interpréteur de commandes a affecté à votre dossier racine et ajoutez les structures **SHITEMID** nécessaires pour vous faire passer du dossier racine à l’objet.

### <a name="interpreting-pidls"></a>Interprétation des PIDL

Lorsque l’interpréteur de commandes ou une application appelle l’une des interfaces de votre extension pour demander des informations sur un objet, il identifie généralement l’objet par un PIDL. Certaines méthodes, telles que [**IShellFolder :: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), utilisent des PIDL relatives au dossier parent et sont faciles à interpréter. Toutefois, votre extension recevra probablement également des PIDL qualifiés complets. Votre gestionnaire PIDL doit ensuite déterminer à quel objet PIDL fait référence.

Ce qui complique la tâche d’association d’un objet à un PIDL qualifié complet, c’est qu’une ou plusieurs des structures [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) initiales dans le PIDL peuvent appartenir à des objets qui se trouvent en dehors de votre extension dans l’espace de noms Shell. Vous n’avez aucun moyen d’interpréter la signification du membre *abID* de ces structures. Ce que votre extension doit faire consiste à « parcourir » la liste des structures **SHITEMID** , jusqu’à ce que vous atteigniez la structure qui correspond à votre dossier racine. À partir de là, vous saurez comment interpréter les informations dans les structures **SHITEMID** .

Pour parcourir le PIDL, prenez la première valeur *CB* et ajoutez-la à l’adresse du PIDL pour avancer le pointeur vers le début de la structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) suivante. Il pointe ensuite vers le membre *CB* de cette structure, que vous pouvez utiliser pour avancer le pointeur vers le début de la structure **SHITEMID** suivante, et ainsi de suite. Chaque fois que vous avancez le pointeur, examinez la structure **SHITEMID** pour déterminer si vous avez atteint la racine de l’espace de noms de votre extension.

## <a name="implementing-the-primary-interfaces"></a>Implémentation des interfaces principales

Comme avec tous les objets COM, l’implémentation d’une extension consiste principalement à implémenter une collection d’interfaces. Cette section présente les trois interfaces principales qui doivent être implémentées par toutes les extensions. elles sont utilisées pour l’initialisation et pour fournir à Windows Explorer des informations de base sur le contenu de l’extension. Ces interfaces, ainsi qu’une [vue de dossier](../lwef/nse-folderview.md), sont toutes nécessaires pour une extension fonctionnelle. toutefois, pour exploiter pleinement les fonctionnalités de l’explorateur de Windows, la plupart des extensions implémentent également une ou plusieurs des interfaces facultatives.

### <a name="ipersistfolder-interface"></a>Interface IPersistFolder

L’interface [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) est appelée pour initialiser un nouvel objet dossier. La méthode [**IPersistFolder :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) assigne un PIDL qualifié complet au nouvel objet. Stockez ce PIDL pour une utilisation ultérieure. Par exemple, un objet dossier doit utiliser ce PIDL pour construire des PIDL qualifiés complets pour les enfants de l’objet. Le créateur de l’objet Folder peut également appeler [**IPersist :: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) pour demander le CLSID de l’objet.

En règle générale, un objet dossier est créé et initialisé par la méthode [**IShellFolder :: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) de son dossier parent. toutefois, lorsqu’un utilisateur accède à votre extension, Windows Explorer crée et initialise l’objet dossier racine de l’extension. Le PIDL que l’objet dossier racine reçoit via [**IPersistFolder :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) contient le chemin d’accès du bureau au dossier racine dont vous aurez besoin pour construire un PIDL complet pour votre extension.

### <a name="ishellfolder-interface"></a>Interface IShellFolder

L’interpréteur de commandes traite une extension comme une collection hiérarchique d’objets Folder. L’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) est le cœur de toute implémentation d’extension. il représente un objet folder et fournit Windows Explorer avec la plupart des informations nécessaires pour afficher le contenu du dossier.

[**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) est généralement la seule interface de dossier autre que [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) qui est directement exposée par un objet Folder. si Windows Explorer utilise une variété d’interfaces obligatoires et facultatives pour obtenir des informations sur le contenu du dossier, il obtient des pointeurs vers ces interfaces via **IShellFolder**.

Windows L’Explorateur obtient le CLSID du dossier racine de votre extension de différentes façons. Pour plus d’informations, consultez [spécification de l’emplacement d’une extension d’espace de noms](nse-junction.md) ou affichage [d’un Self-Contained vue d’une extension d’espace de noms](nse-view.md). Windows L’Explorateur utilise ensuite ce CLSID pour créer et initialiser une instance du dossier racine et pour effectuer une requête pour une interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Votre extension crée un objet dossier pour représenter le dossier racine et retourne l’interface **IShellFolder** de l’objet. la plupart du reste de l’interaction entre votre extension et Windows Explorer s’effectuent alors via **IShellFolder**. Windows L’Explorateur appelle **IShellFolder** pour :

-   Demandez un objet qui peut énumérer le contenu du dossier racine.
-   Obtenez différents types d’informations sur le contenu du dossier racine.
-   Demandez un objet qui expose l’une des interfaces facultatives. Ces interfaces peuvent ensuite être interrogées pour obtenir des informations supplémentaires, telles que des icônes ou des menus contextuels.
-   Demandez un objet dossier qui représente un sous-dossier du dossier racine.

lorsqu’un utilisateur ouvre un sous-dossier du dossier racine, Windows Explorer appelle [**IShellFolder :: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject). Votre extension crée et initialise un nouvel objet dossier pour représenter le sous-dossier et retourne son interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Windows l’explorateur appelle ensuite cette interface pour différents types d’informations, et ainsi de suite jusqu’à ce que l’utilisateur décide de naviguer ailleurs dans l’espace de noms de l’interpréteur de commandes ou de fermer l’explorateur de Windows.

Le reste de cette section décrit brièvement les méthodes [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) les plus importantes et comment les implémenter.

### <a name="enumobjects"></a>EnumObjects

avant d’afficher le contenu d’un dossier dans l’arborescence, Windows Explorer doit d’abord déterminer ce que contient le dossier en appelant la méthode [**IShellFolder :: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) . Cette méthode crée un objet énumération OLE standard qui expose une interface [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) et retourne ce pointeur d’interface. l’interface **IEnumIDList** permet à Windows Explorer d’obtenir le pidl de tous les objets contenus dans le dossier. Ces PIDL sont ensuite utilisés pour obtenir des informations sur les objets contenus dans le dossier. Pour plus d’informations, consultez [IEnumIDList interface](#ienumidlist-interface).

> [!Note]  
> La méthode [**IEnumIDList :: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) ne doit retourner que les PIDL relatifs au dossier parent. Le PIDL doit contenir uniquement la structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) de l’objet, suivie d’un terminateur.

 

### <a name="createviewobject"></a>CreateViewObject

avant d’afficher le contenu d’un dossier, Windows Explorer appelle cette méthode pour demander un pointeur vers une interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . cette interface est utilisée par Windows Explorer pour gérer l’affichage des dossiers. Créez un objet de vue de dossier et retournez son interface **IShellView** .

La méthode [**IShellFolder :: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) est également appelée pour demander l’une des interfaces facultatives, telles que [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), pour le dossier lui-même. Votre implémentation de cette méthode doit créer un objet qui expose l’interface demandée et retourne le pointeur d’interface. si Windows Explorer a besoin d’une interface facultative pour l’un des objets contenus dans le dossier, il appellera [**IShellFolder :: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof).

### <a name="getuiobjectof"></a>GetUIObjectOf

si les informations de base sur le contenu d’un dossier sont disponibles par le biais des méthodes [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) , votre extension peut également fournir Windows Explorer avec différents types d’informations supplémentaires. Par exemple, vous pouvez spécifier des icônes pour le contenu d’un dossier ou le menu contextuel d’un objet. Windows L’Explorateur appelle la méthode [**IShellFolder :: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) pour tenter de récupérer des informations supplémentaires sur un objet contenu dans un dossier. Windows L’Explorateur spécifie l’objet pour lequel il souhaite obtenir des informations, ainsi que l’IID de l’interface appropriée. L’objet Folder crée ensuite un objet qui expose l’interface demandée et retourne le pointeur d’interface.

si votre extension permet aux utilisateurs de transférer des objets avec glisser-déplacer ou le presse-papiers, Windows Explorer appellera [**IShellFolder :: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) pour demander une interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) ou [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Pour plus d’informations, consultez [transfert d’objets Shell avec glisser-déplacer et le presse-papiers](dragdrop.md).

Windows L’Explorateur appelle [**IShellFolder :: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) lorsqu’il souhaite obtenir le même type d’informations sur le dossier lui-même.

### <a name="bindtoobject"></a>BindToObject

Windows L’Explorateur appelle la méthode [**IShellFolder :: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) lorsqu’un utilisateur tente d’ouvrir l’un des sous-dossiers de votre extension. Si *riid* a la valeur IID \_ IShellFolder, vous devez créer et initialiser un objet Folder qui représente le sous-dossier et retourner l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de l’objet.

> [!Note]  
> à l’heure actuelle, Windows Explorer appelle cette méthode uniquement pour demander une interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Toutefois, ne supposez pas que cela sera toujours le cas. Vous devez toujours vérifier la valeur de *riid* avant de continuer.

 

### <a name="getdisplaynameof"></a>GetDisplayNameOf

Windows L’Explorateur appelle la méthode [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) pour convertir le PIDL de l’un des objets du dossier en un nom. Ce PIDL doit être relatif au dossier parent de l’objet. En d’autres termes, il doit contenir une seule structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) non null. comme il existe plusieurs façons de nommer des objets, Windows Explorer spécifie le type de nom en définissant un ou plusieurs indicateurs [**SHGDNF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf) dans le paramètre *uFlags* . L’une des deux valeurs, **SHGDN \_ normal** ou **SHGDN \_ InFolder**, sera définie pour spécifier si le nom doit être relatif au dossier ou relatif au bureau. L’une des trois autres valeurs, **SHGDN \_ FOREDITING**, **SHGDN \_ FORADDRESSBAR** ou **SHGDN \_ FORPARSING**, peut être définie pour spécifier ce à quoi le nom sera utilisé.

Vous devez retourner le nom sous la forme d’une structure [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Si **SHGDN \_ FOREDITING**, **SHGDN \_ FORADDRESSBAR** et **SHGDN \_ FORPARSING** ne sont pas définis, retourne le nom complet de l’objet. si l’indicateur **SHGDN \_ FORPARSING** est défini, Windows Explorer demande un nom d’analyse. Les noms d’analyse sont passés à [**IShellFolder ::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) pour obtenir le PIDL d’un objet, même s’il peut être localisé un ou plusieurs niveaux sous le dossier actif dans la hiérarchie d’espaces de noms. Par exemple, le nom d’analyse d’un objet de système de fichiers est son chemin d’accès. Vous pouvez transmettre le chemin d’accès complet d’un objet du système de fichiers à la méthode **IShellFolder ::P arsedisplayname** du bureau, et il retourne le PIDL complet de l’objet.

Tandis que les noms d’analyse sont des chaînes de texte, ils n’ont pas nécessairement besoin d’inclure le nom complet. Vous devez assigner des noms d’analyse en fonction de ce qui fonctionne le plus efficacement quand [**IShellFolder ::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) est appelée. Par exemple, la plupart des dossiers virtuels de l’interpréteur de commandes ne font pas partie du système de fichiers et n’ont pas de chemin d’accès complet. Au lieu de cela, un GUID est attribué à chaque dossier et le nom d’analyse prend la forme suivante :: {GUID}. Quel que soit le modèle que vous utilisez, il doit pouvoir « aller-retour » de manière fiable. Par exemple, si un appelant passe un nom d’analyse à **IShellFolder ::P arsedisplayname** pour récupérer le PIDL d’un objet, puis passe ce PIDL à [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) avec l’indicateur **SHGDN \_ FORPARSING** défini, l’appelant doit récupérer le nom d’analyse d’origine.

### <a name="getattributesof"></a>GetAttributesOf

Windows L’Explorateur appelle la méthode [**IShellFolder :: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) pour déterminer les attributs d’un ou plusieurs éléments contenus dans un objet Folder. La valeur de *cidl* indique le nombre d’éléments dans la requête et *aPidl* pointe vers une liste de ses PIDL.

étant donné que le test de certains attributs peut prendre du temps, Windows Explorer limite généralement la requête à un sous-ensemble des indicateurs disponibles en définissant leurs valeurs dans *rfgInOut*. Votre méthode doit tester uniquement les attributs dont les indicateurs sont définis dans *rfgInOut*. Laissez les indicateurs valides définis et effacez le reste. Si plusieurs éléments sont inclus dans la requête, définissez uniquement les indicateurs qui s’appliquent à tous les éléments.

> [!Note]  
> Les attributs doivent être correctement définis pour qu’un élément s’affiche correctement. Par exemple, si un élément est un dossier qui contient des sous-dossiers, vous devez définir l’indicateur **SFGAO \_ HASSUBFOLDER** . dans le cas contraire, Windows Explorer n’affichera pas de signe + en regard de l’icône de l’élément dans l’arborescence.

 

### <a name="parsedisplayname"></a>ParseDisplayName

La méthode [**IShellFolder ::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) est dans une certaine mesure une image miroir de [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). L’utilisation la plus courante de cette méthode consiste à convertir le nom d’analyse d’un objet en PIDL associé. Le nom d’analyse peut faire référence à n’importe quel objet qui se trouve sous le dossier dans la hiérarchie d’espaces de noms. Le PIDL retourné est relatif à l’objet Folder qui expose la méthode et n’est généralement pas complet. En d’autres termes, bien que le PIDL puisse contenir plusieurs structures [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , la première est soit celle de l’objet lui-même, soit le premier sous-dossier du chemin d’accès du dossier à l’objet. L’appelant devra ajouter ce PIDL au PIDL complet du dossier pour obtenir un PIDL qualifié complet pour l’objet.

[**IShellFolder ::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) peut également être appelée pour demander les attributs d’un objet. Étant donné que la détermination de tous les attributs applicables peut prendre du temps, l’appelant ne définit que les indicateurs [**SFGAO \_ xxx**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) qui représentent les informations qui intéressent l’appelant. Vous devez déterminer lequel de ces attributs est vrai pour l’objet et effacer les indicateurs restants.

### <a name="ienumidlist-interface"></a>Interface IEnumIDList

lorsque Windows Explorer doit énumérer les objets contenus dans un dossier, il appelle [**IShellFolder :: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects). L’objet Folder doit créer un objet d’énumération qui expose l’interface [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) et retourner ce pointeur d’interface. Windows L’Explorateur utilise alors généralement **IEnumIDList** pour énumérer les PIDL de tous les objets contenus dans le dossier.

[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) est une interface d’énumération OLE standard et est implémentée de manière habituelle. N’oubliez pas, cependant, que le PIDL que vous retournez doit être relatif au dossier et contenir uniquement la structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) de l’objet et un terminateur.

## <a name="implementing-the-optional-interfaces"></a>Implémentation des interfaces facultatives

Il existe un certain nombre d’interfaces de Shell facultatives que les objets de dossiers de votre extension peuvent prendre en charge. La plupart d’entre eux, tels que [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona), vous permettent de personnaliser différents aspects de la façon dont l’utilisateur affiche votre extension. D’autres, telles que [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject), permettent à votre extension de prendre en charge des fonctionnalités telles que le glisser-déplacer.

Aucune des interfaces facultatives n’est exposée directement par un objet Folder. au lieu de cela, Windows Explorer appelle l’une des deux méthodes [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) pour demander une interface :

-   Windows L’Explorateur appelle le [**IShellFolder :: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) d’un objet Folder pour demander une interface pour l’un des objets contenus dans le dossier.
-   Windows L’Explorateur appelle le [**IShellFolder :: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) d’un objet Folder pour demander une interface pour le dossier lui-même.

Pour fournir les informations, l’objet Folder crée un objet qui expose l’interface demandée et retourne le pointeur d’interface. Windows L’Explorateur appelle ensuite cette interface pour récupérer les informations nécessaires. Cette section décrit les interfaces facultatives les plus couramment utilisées.

### <a name="iextracticon"></a>IExtractIcon

Windows L’Explorateur demande une interface [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) avant d’afficher le contenu d’un dossier. L’interface permet à votre extension de spécifier des icônes personnalisées pour les objets contenus dans le dossier. Dans le cas contraire, les icônes de fichier et de dossier standard seront utilisées. Pour fournir une icône personnalisée, créez un objet d’extraction d’icône qui expose **IExtractIcon** et retournez un pointeur vers cette interface. Pour plus d’informations, consultez la documentation de référence **IExtractIcon** ou [création de gestionnaires d’icône](./how-to-create-icon-handlers.md).

### <a name="icontextmenu"></a>IContextMenu

quand un utilisateur clique avec le bouton droit sur un objet, Windows Explorer demande une interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Pour fournir des menus contextuels pour vos objets, créez un objet gestionnaire de menus et retournez son interface **IContextMenu** .

Les procédures de création d’un objet gestionnaire de menus sont très similaires à celles utilisées pour créer une extension de Shell de gestionnaire de menu. Pour plus d’informations, consultez [création de gestionnaires de menus contextuels](context-menu-handlers.md) ou référence [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)ou [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) .

### <a name="iqueryinfo"></a>IQueryInfo

Windows L’Explorateur appelle l’interface [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) pour récupérer une chaîne de texte info-bulle.

### <a name="idataobject-and-idroptarget"></a>IDataObject et IDropTarget

lorsque vos objets sont affichés par Windows Explorer, un objet folder n’a aucune façon directe de savoir quand un utilisateur tente de couper, copier ou faire glisser un objet. au lieu de cela, Windows Explorer demande une interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) . Pour autoriser le transfert de l’objet, créez un objet de données et retournez un pointeur vers son interface **IDataObject** .

de même, un utilisateur peut tenter de supprimer un objet de données sur une représentation Windows Explorer de l’un de vos objets, tel qu’une icône ou un chemin de barre d’adresses. Windows L’Explorateur demande ensuite une interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Pour autoriser la suppression de l’objet de données, créez un objet qui expose une interface **IDropTarget** et retournez le pointeur d’interface.

Le traitement du transfert de données est l’un des aspects les plus délicats de l’écriture d’extensions d’espace de noms. Pour une présentation détaillée, consultez [transfert d’objets Shell avec glisser-déplacer et le presse-papiers](dragdrop.md).

## <a name="working-with-the-default-shell-folder-view-implementation"></a>Utilisation de l’implémentation de l’affichage des dossiers shell par défaut

Les sources de données qui utilisent l’objet DefView (Shell Folder View) par défaut doivent implémenter les interfaces suivantes :

-   [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)
-   [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2)
-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)
-   [**IPersistFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)

Si vous le souhaitez, ils peuvent également implémenter [**IPersistFolder3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3).

 

 
