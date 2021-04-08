---
title: handle (attribut)
description: L’attribut \ handle \ spécifie un défini par l’utilisateur ou \ 0034 ; personnalisé \ 0034 ; type de handle.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- handle MIDL d’attribut
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842289"
---
# <a name="handle-attribute"></a><span data-ttu-id="a5138-104">handle (attribut)</span><span class="sxs-lookup"><span data-stu-id="a5138-104">handle attribute</span></span>

<span data-ttu-id="a5138-105">L' \[ attribut **handle** \] spécifie un type de handle défini par l’utilisateur ou « personnalisé ».</span><span class="sxs-lookup"><span data-stu-id="a5138-105">The \[**handle**\] attribute specifies a user-defined or "customized" handle type.</span></span>

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a><span data-ttu-id="a5138-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5138-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5138-107">*TypeName*</span><span class="sxs-lookup"><span data-stu-id="a5138-107">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="a5138-108">Spécifie le nom du type de handle de liaison défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5138-108">Specifies the name of the user-defined binding-handle type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5138-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a5138-109">Remarks</span></span>

<span data-ttu-id="a5138-110">Les handles définis par l’utilisateur permettent aux développeurs de concevoir des handles significatifs pour l’application.</span><span class="sxs-lookup"><span data-stu-id="a5138-110">User-defined handles permit developers to design handles that are meaningful to the application.</span></span> <span data-ttu-id="a5138-111">Un descripteur défini par l’utilisateur ne peut être défini que dans une déclaration de type, et non dans un déclarateur de fonction.</span><span class="sxs-lookup"><span data-stu-id="a5138-111">A user-defined handle can only be defined in a type declaration, not in a function declarator.</span></span>

<span data-ttu-id="a5138-112">Un paramètre d’un type défini par l' \[  \] attribut handle est utilisé pour déterminer la liaison de l’appel et est transmis à la procédure appelée.</span><span class="sxs-lookup"><span data-stu-id="a5138-112">A parameter of a type defined by the \[**handle**\] attribute is used to determine the binding for the call and is transmitted to the called procedure.</span></span>

<span data-ttu-id="a5138-113">L’utilisateur doit fournir des routines de liaison et d’annulation de liaison pour la conversion entre les types de handles primitifs et définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5138-113">The user must provide binding and unbinding routines to convert between primitive and user-defined handle types.</span></span> <span data-ttu-id="a5138-114">À partir d’un handle défini par l’utilisateur de type *TypeName*, l’utilisateur doit fournir les routines *TypeName* \_ **Bind** et *TypeName* \_ **Unbind**.</span><span class="sxs-lookup"><span data-stu-id="a5138-114">Given a user-defined handle of type *typename*, the user must supply the routines *typename*\_**bind** and *typename*\_**unbind**.</span></span> <span data-ttu-id="a5138-115">Par exemple, si le type de handle défini par l’utilisateur est nommé MYHANDLE, les routines sont nommées MYHANDLE \_ **Bind** et MYHANDLE \_ **Unbind**.</span><span class="sxs-lookup"><span data-stu-id="a5138-115">For example, if the user-defined handle type is named MYHANDLE, the routines are named MYHANDLE\_**bind** and MYHANDLE\_**unbind**.</span></span>

<span data-ttu-id="a5138-116">En cas de réussite, la routine de liaison *TypeName* \_  doit retourner un handle de liaison primitif valide.</span><span class="sxs-lookup"><span data-stu-id="a5138-116">If successful, the *typename*\_**bind** routine should return a valid primitive binding handle.</span></span> <span data-ttu-id="a5138-117">En cas d’échec, la routine doit retourner une **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a5138-117">If unsuccessful, the routine should return a **NULL**.</span></span> <span data-ttu-id="a5138-118">Si la routine retourne la **valeur null**, la routine *TypeName* \_ **Unbind** ne sera pas appelée.</span><span class="sxs-lookup"><span data-stu-id="a5138-118">If the routine returns **NULL**, the *typename*\_**unbind** routine will not be called.</span></span> <span data-ttu-id="a5138-119">Si la routine de liaison retourne un handle de liaison non valide différent de **null**, le comportement de stub n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="a5138-119">If the binding routine returns an invalid binding handle different from **NULL**, the stub behavior is undefined.</span></span>

<span data-ttu-id="a5138-120">Lorsque la procédure distante a un handle défini par l’utilisateur en tant que paramètre ou qu’un handle implicite, les stubs client appellent la routine de liaison avant d’appeler la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="a5138-120">When the remote procedure has a user-defined handle as a parameter or as an implicit handle, the client stubs call the binding routine before calling the remote procedure.</span></span> <span data-ttu-id="a5138-121">Les stubs client appellent la routine d’annulation de liaison après l’appel distant.</span><span class="sxs-lookup"><span data-stu-id="a5138-121">The client stubs call the unbinding routine after the remote call.</span></span>

<span data-ttu-id="a5138-122">Dans un IDL DCE, un paramètre avec l' \[  \] attribut handle doit apparaître comme premier paramètre dans la liste d’arguments de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="a5138-122">In DCE IDL, a parameter with the \[**handle**\] attribute must appear as the first parameter in the remote procedure argument list.</span></span> <span data-ttu-id="a5138-123">Les paramètres suivants, y compris les autres \[  \] attributs de handle, sont traités comme des paramètres ordinaires.</span><span class="sxs-lookup"><span data-stu-id="a5138-123">Subsequent parameters, including other \[**handle**\] attributes, are treated as ordinary parameters.</span></span> <span data-ttu-id="a5138-124">Microsoft prend en charge une extension de l’IDL DCE qui permet d’afficher le paramètre de handle défini par l’utilisateur \[  \] dans des positions autres que le premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="a5138-124">Microsoft supports an extension to DCE IDL that allows the user-defined \[**handle**\] parameter to appear in positions other than the first parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="a5138-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="a5138-125">Examples</span></span>

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a><span data-ttu-id="a5138-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5138-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5138-127">Liaison et Handles</span><span class="sxs-lookup"><span data-stu-id="a5138-127">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="a5138-128">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="a5138-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a5138-129">**handle implicite \_**</span><span class="sxs-lookup"><span data-stu-id="a5138-129">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="a5138-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="a5138-130">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 