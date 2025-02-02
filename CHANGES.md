# Changelog

## v. 0.3.2
 * fix: Dummy logger class

## v. 0.3.1
 * fix: ensure loaded PiiCollection objects have integer ids for Detectors
 * fix: only add lang to PiiCollection header if defined
 
## v. 0.3.0
 * PiiEntityInfo made immutable
 * added clone() class method to PiiCollection
 * refactored & improved config reading
 * new functionality in helper.io: read remote files
 * json dump parameters modified
    - allow no-indent specification
    - only close output file if we opened it
    - allow additional formatting arguments
 * added logger wrapper

## v. 0.2.0
 * DocumentChunk class refactored into a full class, with equality method and
   asdict()
 * Refactored dump code; dump to JSON
 * when dumping documents to JSON & YAML dump non-structural context fields
   (and skip structural context)
 * modified tree & sequence iteration: changed automatic id assignment
 * new class method from_dict() in PiiInstance
 * when reading a PiiCollection from file, recreate PiiInstance objects
 * wrapper load() method for PiiCollectionLoader
 * add_chunk() method for LocalSrcDocument objects (sequence, table & tree)
 * new LocalSrcDocumentFile dispatcher class
 * openfile: allow file-like objects as argument
 * fixed newlines in text output
 * added json dump to object
 * added config file management
 * new PiiEnum values
 * refactored PiiEntity; new PiiEntityInfo subclass
 * special SrcDocument metadata field "default_lang"
 * added "lang" context field to DocumentChunk, automatically copied from
   document "default_lang" if not present
 * some bugfixes

## v. 0.1.0
 * updated for data spec 0.4.0
 * added two iterators
    - iter_full, including iteration with context
    - iter_struct
 * renamed SourceDocument to SrcDocument
 * local load/dump split from SrcDocument, into a LocalSrcDocument class +
   a module function
 * added base classes for table, tree & sequence docs
 * chunk payload change from `text` to `data`, to make it more generic
 * added format indicator strings to output dump

## v. 0.0.3
 * added BaseSourceDocument and BaseSourceDocument classes
 * minor fixes in other data structures
