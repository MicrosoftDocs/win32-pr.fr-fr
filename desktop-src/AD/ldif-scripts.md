---
title: Scripts LDIF
description: Le format LDIF (LDAP Data Interchange Format) est une norme IETF (Internet Engineering Task Force) qui définit l’importation et l’exportation des données d’annuaire entre les serveurs d’annuaire qui utilisent des fournisseurs de services LDAP.
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- Active Directory de scripts LDIF
- Scripts LDIF Active Directory, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e228e48770e1190065a16c95b4011f794127fbdd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103940707"
---
# <a name="ldif-scripts"></a><span data-ttu-id="57f26-105">Scripts LDIF</span><span class="sxs-lookup"><span data-stu-id="57f26-105">LDIF Scripts</span></span>

<span data-ttu-id="57f26-106">Le format LDIF (LDAP Data Interchange Format) est une norme IETF (Internet Engineering Task Force) qui définit l’importation et l’exportation des données d’annuaire entre les serveurs d’annuaire qui utilisent des fournisseurs de services LDAP.</span><span class="sxs-lookup"><span data-stu-id="57f26-106">The LDAP Data Interchange Format (LDIF) is an Internet Engineering Task Force (IETF) standard that defines how to import and export directory data between directory servers that use LDAP service providers.</span></span> <span data-ttu-id="57f26-107">Windows 2000 et Windows Server 2003 incluent un utilitaire de ligne de commande, LDIFDE, qui peut être utilisé pour importer des objets d’annuaire dans Active Directory Domain Services à l’aide de fichiers LDIF.</span><span class="sxs-lookup"><span data-stu-id="57f26-107">Windows 2000 and Windows Server 2003 include a command-line utility, LDIFDE, which can be used to import directory objects into Active Directory Domain Services using LDIF files.</span></span> <span data-ttu-id="57f26-108">LDIFDE vous permet de définir un filtre sur une chaîne spécifique afin de rechercher et de répertorier les objets d’annuaire dans Active Directory Domain Services en tant que fichiers LDIF pouvant être facilement lus par les administrateurs de schéma.</span><span class="sxs-lookup"><span data-stu-id="57f26-108">LDIFDE enables you to set a filter to a specific string in order to search for and list directory objects in Active Directory Domain Services as LDIF files which can be easily read by schema administrators.</span></span>

<span data-ttu-id="57f26-109">Lors de l’importation d’un fichier Unicode, LDIFDE importe le fichier au format Unicode s’il contient l’identificateur Unicode au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="57f26-109">When importing a Unicode file, LDIFDE imports the file as Unicode if it contains the Unicode identifier at the beginning of the file.</span></span> <span data-ttu-id="57f26-110">Si vous souhaitez importer un fichier au format Unicode lorsqu’il ne contient pas l’identificateur Unicode au début du fichier, vous pouvez utiliser le commutateur-u afin de le forcer à être importé au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="57f26-110">If you wish to import a file as Unicode when it does not contain the Unicode identifier at the beginning of the file, you can use the -u switch in order to force it to be imported as Unicode.</span></span>

<span data-ttu-id="57f26-111">Le mode par défaut pour l’exportation des fichiers est ANSI.</span><span class="sxs-lookup"><span data-stu-id="57f26-111">The default mode for exporting files is ANSI.</span></span> <span data-ttu-id="57f26-112">S’il existe des entrées Unicode, elles sont converties au format 64 de base.</span><span class="sxs-lookup"><span data-stu-id="57f26-112">If there are Unicode entries, they will be converted into base 64 format.</span></span> <span data-ttu-id="57f26-113">Pour exporter un fichier au format Unicode, utilisez le commutateur-u.</span><span class="sxs-lookup"><span data-stu-id="57f26-113">To export a file into Unicode format, use the -u switch.</span></span>

<span data-ttu-id="57f26-114">Un fichier LDIF doit appliquer des modifications de schéma lorsqu’il existe des dépendances entre les attributs qui sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="57f26-114">An LDIF file must apply schema changes when there are dependencies between the attributes that are added.</span></span> <span data-ttu-id="57f26-115">Par exemple, les attributs de lien suivant doivent être ajoutés avant l’attribut de lien précédent correspondant.</span><span class="sxs-lookup"><span data-stu-id="57f26-115">For example, forward link attributes should be added before the corresponding back link attribute.</span></span> <span data-ttu-id="57f26-116">Vous devez également mettre à jour le cache de schéma avant d’ajouter des classes qui dépendent des attributs ou des classes ajoutées précédemment dans le script LDIF.</span><span class="sxs-lookup"><span data-stu-id="57f26-116">You must also update the schema cache before adding classes that depend on attributes or classes added earlier in the LDIF script.</span></span> <span data-ttu-id="57f26-117">Pour plus d’informations, consultez l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="57f26-117">For more information, see the following code example.</span></span>

<span data-ttu-id="57f26-118">N’oubliez pas que pour les valeurs binaires, vous devez encoder les valeurs au format Base64.</span><span class="sxs-lookup"><span data-stu-id="57f26-118">Be aware that for binary values, you must encode the values as base64.</span></span> <span data-ttu-id="57f26-119">L’encodage Base64 est défini dans la norme IETF RFC 2045, section 6,8.</span><span class="sxs-lookup"><span data-stu-id="57f26-119">Base64 encoding is defined in IETF RFC 2045, Section 6.8.</span></span>

<span data-ttu-id="57f26-120">Pour plus d’informations sur le format des fichiers LDIF, consultez [LDAP Data Interchange Format (LDIF)-Technical Specification](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) sur le site Web de l’IETF (Internet Engineering Task Force).</span><span class="sxs-lookup"><span data-stu-id="57f26-120">For more information about the format of LDIF files, see [The LDAP Data Interchange Format (LDIF) - Technical Specification](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) on the Internet Engineering Task Force website.</span></span>

## <a name="ntds-specific-ldif-changetypes"></a><span data-ttu-id="57f26-121">ChangeTypes LDIF spécifique à NTDS</span><span class="sxs-lookup"><span data-stu-id="57f26-121">NTDS-specific LDIF changetypes</span></span>

<span data-ttu-id="57f26-122">Il est préférable d’utiliser ntdsSchema \* ChangeTypes au lieu d’appeler LDIFDE-k.</span><span class="sxs-lookup"><span data-stu-id="57f26-122">It is better to use ntdsSchema\* changetypes rather than calling ldifde -k.</span></span> <span data-ttu-id="57f26-123">L’option-k de LDIFDE ignore un plus grand ensemble d’erreurs LDAP.</span><span class="sxs-lookup"><span data-stu-id="57f26-123">The -k option of ldifde ignores a larger set of LDAP errors.</span></span> <span data-ttu-id="57f26-124">La liste complète des erreurs ignorées est la suivante :</span><span class="sxs-lookup"><span data-stu-id="57f26-124">The complete list of ignored errors is as follows:</span></span>

-   <span data-ttu-id="57f26-125">L’objet est déjà membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="57f26-125">The object is already a member of the group.</span></span>
-   <span data-ttu-id="57f26-126">Une violation de classe d’objet (c’est-à-dire que la classe d’objet spécifiée n’existe pas), si l’objet en cours d’importation n’a pas d’autres attributs.</span><span class="sxs-lookup"><span data-stu-id="57f26-126">An object class violation (meaning the specified object class does not exist), if the object being imported has no other attributes.</span></span>
-   <span data-ttu-id="57f26-127">l’objet existe déjà **( \_ LDAP \_ existe déjà**)</span><span class="sxs-lookup"><span data-stu-id="57f26-127">object already exists (**LDAP\_ALREADY\_EXISTS**)</span></span>
-   <span data-ttu-id="57f26-128">violation de contrainte **( \_ \_ violation de contrainte LDAP**)</span><span class="sxs-lookup"><span data-stu-id="57f26-128">constraint violation (**LDAP\_CONSTRAINT\_VIOLATION**)</span></span>
-   <span data-ttu-id="57f26-129">l’attribut ou la valeur existe déjà (**\_ attribut \_ ou \_ valeur \_ LDAP**)</span><span class="sxs-lookup"><span data-stu-id="57f26-129">attribute or value already exists (**LDAP\_ATTRIBUTE\_OR\_VALUE\_EXISTS**)</span></span>
-   <span data-ttu-id="57f26-130">aucun objet de ce type (**LDAP \_ non- \_ \_ objet de ce type**)</span><span class="sxs-lookup"><span data-stu-id="57f26-130">no such object (**LDAP\_NO\_SUCH\_OBJECT**)</span></span>

<span data-ttu-id="57f26-131">Les ChangeTypes suivants sont conçus spécifiquement pour les opérations de mise à niveau de schéma.</span><span class="sxs-lookup"><span data-stu-id="57f26-131">The following changetypes are designed specifically for schema upgrade operations.</span></span>



| <span data-ttu-id="57f26-132">ChangeType</span><span class="sxs-lookup"><span data-stu-id="57f26-132">Changetype</span></span>                      | <span data-ttu-id="57f26-133">Description</span><span class="sxs-lookup"><span data-stu-id="57f26-133">Description</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57f26-134">**ntdsSchemaAdd**</span><span class="sxs-lookup"><span data-stu-id="57f26-134">**ntdsSchemaAdd**</span></span><br/>    | <span data-ttu-id="57f26-135">**ntdsSchemaAdd** correspond à **Ajouter** dans un fichier LDIF.</span><span class="sxs-lookup"><span data-stu-id="57f26-135">**ntdsSchemaAdd** corresponds to **add** in an LDIF file.</span></span> <span data-ttu-id="57f26-136">La seule différence est que **ntdsSchemaAdd** ferait en sorte que LDIFDE ignore une opération d' **Ajout** si l’objet existe déjà dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="57f26-136">The only difference is that **ntdsSchemaAdd** would cause ldifde to skip an **add** operation if the object already exists in the schema.</span></span> <span data-ttu-id="57f26-137">(**LDAP \_ \_ existe déjà** est ignoré.)</span><span class="sxs-lookup"><span data-stu-id="57f26-137">(**LDAP\_ALREADY\_EXISTS** is ignored.)</span></span><br/>                                   |
| <span data-ttu-id="57f26-138">**ntdsSchemaModify**</span><span class="sxs-lookup"><span data-stu-id="57f26-138">**ntdsSchemaModify**</span></span><br/> | <span data-ttu-id="57f26-139">**ntdsSchemaModify** correspond à **modifier** dans un fichier LDIF.</span><span class="sxs-lookup"><span data-stu-id="57f26-139">**ntdsSchemaModify** corresponds to **modify** in an LDIF file.</span></span> <span data-ttu-id="57f26-140">La seule différence est que **ntdsSchemaModify** ferait en sorte que LDIFDE ignore une opération de **modification** si l’objet est introuvable dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="57f26-140">The only difference is that **ntdsSchemaModify** would cause ldifde to skip an **modify** operation if the object is not found in the schema.</span></span> <span data-ttu-id="57f26-141">(**LDAP \_ non \_ , cet \_ objet** n’est pas pris en compte.)</span><span class="sxs-lookup"><span data-stu-id="57f26-141">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="57f26-142">**ntdsSchemaDelete**</span><span class="sxs-lookup"><span data-stu-id="57f26-142">**ntdsSchemaDelete**</span></span><br/> | <span data-ttu-id="57f26-143">**ntdsSchemaDelete** correspond à **Delete** dans un fichier LDIF.</span><span class="sxs-lookup"><span data-stu-id="57f26-143">**ntdsSchemaDelete** corresponds to **delete** in an LDIF file.</span></span> <span data-ttu-id="57f26-144">La seule différence est que **ntdsSchemaDelete** ferait en sorte que LDIFDE ignore une opération de **suppression** si l’objet est introuvable dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="57f26-144">The only difference is that **ntdsSchemaDelete** would cause ldifde to skip an **delete** operation if the object is not found in the schema.</span></span> <span data-ttu-id="57f26-145">(**LDAP \_ non \_ , cet \_ objet** n’est pas pris en compte.)</span><span class="sxs-lookup"><span data-stu-id="57f26-145">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="57f26-146">**ntdsSchemaModRdn**</span><span class="sxs-lookup"><span data-stu-id="57f26-146">**ntdsSchemaModRdn**</span></span><br/> | <span data-ttu-id="57f26-147">**ntdsSchemaModRdn** correspond à **modrdn** dans un fichier LDIF.</span><span class="sxs-lookup"><span data-stu-id="57f26-147">**ntdsSchemaModRdn** corresponds to **modrdn** in an LDIF file.</span></span> <span data-ttu-id="57f26-148">La seule différence est que **ntdsSchemaModRdn** ferait en sorte que LDIFDE ignore une opération de modification relative à un nom unique si l’objet est introuvable dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="57f26-148">The only difference is that **ntdsSchemaModRdn** would cause ldifde to skip a modify-relative-distinguished-name operation if the object is not found in the schema.</span></span> <span data-ttu-id="57f26-149">(**LDAP \_ non \_ , cet \_ objet** n’est pas pris en compte.)</span><span class="sxs-lookup"><span data-stu-id="57f26-149">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/> |



 

## <a name="example"></a><span data-ttu-id="57f26-150">Exemple</span><span class="sxs-lookup"><span data-stu-id="57f26-150">Example</span></span>

<span data-ttu-id="57f26-151">L’exemple de code suivant comprend :</span><span class="sxs-lookup"><span data-stu-id="57f26-151">The following code example includes:</span></span>

-   <span data-ttu-id="57f26-152">Myschemaext. ldf est un script LDIF qui contient de nouveaux attributs et classes.</span><span class="sxs-lookup"><span data-stu-id="57f26-152">Myschemaext.ldf is an LDIF script that contains new attributes and classes.</span></span> <span data-ttu-id="57f26-153">Sachez que ce fichier est une version modifiée du fichier généré à partir de Lgetattcls.vbs.</span><span class="sxs-lookup"><span data-stu-id="57f26-153">Be aware that this file is a modified version of the file generated from Lgetattcls.vbs.</span></span> <span data-ttu-id="57f26-154">Sachez également que l’attribut **My-test-attribute-DN-FL** a été déplacé en avance de **My-test-attribute-DN-BL** , car le lien de retour (**My-test-attribute-DN-BL**) dépend du lien suivant (**My-test-attribute-DN-FL**).</span><span class="sxs-lookup"><span data-stu-id="57f26-154">Also be aware that the **My-Test-Attribute-DN-FL** attribute was moved ahead of **My-Test-Attribute-DN-BL** because the back link (**My-Test-Attribute-DN-BL**) is dependent on the forward link (**My-Test-Attribute-DN-FL**).</span></span> <span data-ttu-id="57f26-155">En outre, l’attribut opérationnel **schemaUpdateNow** est défini à deux emplacements pour déclencher les mises à jour du cache de schéma afin que les classes et attributs dépendants soient disponibles pour l’ajout des deux classes dans le script.</span><span class="sxs-lookup"><span data-stu-id="57f26-155">Furthermore, the **schemaUpdateNow** operational attribute is set in two places to trigger updates of the schema cache so that dependent attributes and classes will be available for adding the two classes in the script.</span></span>
    > [!Note]  
    > <span data-ttu-id="57f26-156">Consultez la rubrique [obtention d’un ID de lien](obtaining-a-link-id.md) pour plus d’informations sur la source de l’ID dans les instructions LinkId :.</span><span class="sxs-lookup"><span data-stu-id="57f26-156">See the topic [Obtaining a Link ID](obtaining-a-link-id.md) for information about the source of the ID in the linkID: statements.</span></span>

     

-   <span data-ttu-id="57f26-157">Lgetattcls.vbs est un fichier VBScript qui génère le script LDIF utilisé comme point de départ pour Myschemaext. ldf.</span><span class="sxs-lookup"><span data-stu-id="57f26-157">Lgetattcls.vbs is a VBScript file that generates the LDIF script used as the starting point for the Myschemaext.ldf.</span></span> <span data-ttu-id="57f26-158">N’oubliez pas que le chemin d’accès au schéma actuel est remplacé par CN = Schema, CN = Configuration, DC = myorg, DC = com.</span><span class="sxs-lookup"><span data-stu-id="57f26-158">Be aware that the current schema path is replaced by CN=Schema,CN=Configuration,DC=myorg,DC=com.</span></span> <span data-ttu-id="57f26-159">Vous pouvez remplacer DC = myorg, DC = com pour qu’il reflète le nom unique (DN) à publier dans le script LDIF, en vous assurant que LSETATTCLS.VBS reflète la modification apportée à son **sFromDN** de sorte que le nom de domaine correct soit remplacé lors de l’application du script LDIF.</span><span class="sxs-lookup"><span data-stu-id="57f26-159">You can replace DC=myorg,DC=com to reflect the distinguished name (DN) to publish in the LDIF script  ensure that LSETATTCLS.VBS reflects the change in its **sFromDN** so that the correct DN is replaced when the LDIF script is applied.</span></span> <span data-ttu-id="57f26-160">Sachez également que le script utilise un préfixe pour rechercher les classes et les attributs. vous devez également définir et utiliser un préfixe pour l’ensemble de vos classes et attributs.</span><span class="sxs-lookup"><span data-stu-id="57f26-160">Also be aware that the script uses a prefix to find the classes and attributes you should also define and use a prefix for all your classes and attributes.</span></span> <span data-ttu-id="57f26-161">Pour plus d’informations, consultez [affectation de noms aux classes et attributs](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="57f26-161">For more information, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span> <span data-ttu-id="57f26-162">En outre, le script génère uniquement les attributs nécessaires pour les objets **attributeSchema** et **classSchema** dans le fichier LDIF.</span><span class="sxs-lookup"><span data-stu-id="57f26-162">In addition, the script outputs only the necessary attributes for the **attributeSchema** and **classSchema** objects to the LDIF file.</span></span>
-   <span data-ttu-id="57f26-163">Lsetattcls.vbs est un fichier VBScript qui utilise le script Myschemaext. ldf pour ajouter les nouveaux attributs et classes du script.</span><span class="sxs-lookup"><span data-stu-id="57f26-163">Lsetattcls.vbs is a VBScript file that uses the Myschemaext.ldf script to add the new attributes and classes in the script.</span></span> <span data-ttu-id="57f26-164">Assurez-vous que le contrôleur de schéma est en mesure d’écrire dans avant d’exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="57f26-164">Ensure that the schema master is able to be written to before running the script.</span></span>

## <a name="myschemaextldf"></a><span data-ttu-id="57f26-165">MYSCHEMAEXT. LDF</span><span class="sxs-lookup"><span data-stu-id="57f26-165">MYSCHEMAEXT.LDF</span></span>

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a><span data-ttu-id="57f26-166">LGETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="57f26-166">LGETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a><span data-ttu-id="57f26-167">LSETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="57f26-167">LSETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 





